# User Metrics Measurement Guide

This guide documents how Blackbird measures user metrics based on production KPI queries.

---

## Core Tables for User Metrics

### Primary User Identity

```
users
  └── user_id (UUID) - Primary user identifier
```

### User Activity Tracking

```
check_ins
  ├── user_id → users.user_id
  ├── location_id → locations.location_id
  ├── membership_id → memberships.membership_id
  ├── nfc_chip_id → nfc_chips.nfc_chip_id
  └── created_at (timestamp for daily metrics)
```

### Transaction Tracking

```
check_shares
  ├── user_id → users.user_id
  ├── check_id → checks.check_id
  └── check_share_total (payment amount)

checks
  ├── location_id → locations.location_id
  ├── status (filter for 'CLOSED')
  └── paid_at (timestamp for TPV)

payments
  ├── check_share_id → check_shares.check_share_id
  ├── amount
  └── status
```

---

## Key Metric Definitions

### DAU (Daily Active Users)

**Definition:** Count of unique users with activity on a given day

**Activity Types Counted:**

- Check-ins at locations
- Membership claims
- Collaboration claims
- Messages sent
- Activation events

**SQL Pattern:**

```sql
-- Unique users with check-ins
SELECT
  DATE(check_ins.created_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT user_id) AS dau
FROM check_ins
WHERE DATE(created_at AT TIME ZONE 'America/New_York') = 'YYYY-MM-DD'
GROUP BY 1
```

### Check-ins

**Definition:** Total number of check-in events (not unique users)

**SQL Pattern:**

```sql
SELECT
  DATE(check_ins.created_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT check_in_id) AS check_ins
FROM check_ins
  LEFT JOIN nfc_chips ON nfc_chips.nfc_chip_id = check_ins.nfc_chip_id
GROUP BY 1
```

### Unique Paying Users

**Definition:** Distinct users who completed a payment

**SQL Pattern:**

```sql
SELECT
  DATE(checks.paid_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT check_shares.user_id) AS paying_users
FROM check_shares
  LEFT JOIN checks ON checks.check_id = check_shares.check_id
WHERE checks.status = 'CLOSED'
GROUP BY 1
```

### TPV (Total Payment Volume)

**Definition:** Sum of all payment amounts in dollars

**Components:**

- Check share payments (card + wallet)
- FLY redemptions
- Collaboration purchases
- Payment links
- PDR (Private Dining Room) deposits and charges

**Key Tables for TPV:**

```
check_share_payments    - Card payments on checks
check_share_fly_redemptions - FLY token redemptions
collab_purchases        - Collaboration purchases
collab_fly_redemptions  - FLY used on collabs
payment_links           - Direct payment links
pdr_deposit             - Private dining deposits
pdr_final_charge        - Private dining final charges
```

### Downloads

**Definition:** App installs tracked via users.created_at

**SQL Pattern:**

```sql
SELECT
  DATE(users.created_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT user_id) AS downloads
FROM users
GROUP BY 1
```

---

## Table Relationships for User Metrics

```
users
  │
  ├──< memberships (user_id)
  │      └──< check_ins (membership_id)
  │
  ├──< check_ins (user_id)
  │      ├── location_id → locations
  │      └── nfc_chip_id → nfc_chips
  │
  ├──< check_shares (user_id)
  │      ├── check_id → checks
  │      │      └── location_id → locations
  │      └──< payments (via check_share_id)
  │
  ├──< cards (user_id)
  │
  ├──< conversation_messages (user_id)
  │
  └──< fly_ledger_entries (user_id)
```

---

## Location Hierarchy

```
restaurants
  └──< locations (restaurant_id)
         ├── neighborhood_id → neighborhoods
         └──< nfc_chips (location_id)
                └──< check_ins (nfc_chip_id)
```

---

## Common Filters

### Time Zone

All daily metrics use Eastern Time:

```sql
AT TIME ZONE 'America/New_York'
```

### Live Locations Only

```sql
WHERE locations.status = 'LIVE'
```

### Closed Checks Only

```sql
WHERE checks.status = 'CLOSED'
```

### Exclude Employees

Employee check-ins are typically filtered via:

```sql
WHERE check_ins.initiation_type != 'EMPLOYEE'
-- or via nfc_chip relationship
```

---

## Comparison Patterns

### Yesterday vs Trailing 4-Week Average

This is a common pattern across KPIs:

```sql
WITH prior_weekdays AS (
  -- Get same day-of-week for past 4 weeks
  SELECT generate_series(1, 4) AS week_offset
),
prior_values AS (
  SELECT AVG(metric_value) as trailing_avg
  FROM metrics
  WHERE date IN (
    SELECT (CURRENT_DATE - INTERVAL '1 day') - (week_offset * 7)
    FROM prior_weekdays
  )
)
SELECT
  yesterday_value,
  trailing_avg,
  (yesterday_value - trailing_avg) / trailing_avg * 100 AS pct_change
```

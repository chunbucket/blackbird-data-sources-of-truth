# Market-Level Metrics Guide

This guide documents how to query market-level data in the Blackbird production database.

---

## Geographic Hierarchy

```
neighborhoods.city (Market)
       │
neighborhoods (Neighborhood/Area)
       │
locations (Individual Venue)
       │
restaurants (Parent Entity)
```

---

## Key Tables

### `neighborhoods`

| Column          | Type        | Description                                     |
| --------------- | ----------- | ----------------------------------------------- |
| neighborhood_id | uuid        | Primary key                                     |
| name            | text        | Neighborhood name (e.g., "SoHo", "Mission Bay") |
| city            | text        | **THE MARKET FIELD**                            |
| created_at      | timestamptz |                                                 |
| updated_at      | timestamptz |                                                 |

### `locations`

| Column          | Type    | Description                                            |
| --------------- | ------- | ------------------------------------------------------ |
| location_id     | uuid    | Primary key                                            |
| neighborhood_id | uuid    | FK → neighborhoods                                     |
| restaurant_id   | uuid    | FK → restaurants                                       |
| live            | boolean | **Use this for live status (NOT a status column)**     |
| city            | text    | Location's city (less reliable than neighborhood.city) |
| state           | text    |                                                        |
| zipcode         | text    |                                                        |

---

## Active Markets

### Primary Markets (50+ Live Locations)

| Market        | Live Locations | Notes                                     |
| ------------- | -------------- | ----------------------------------------- |
| New York      | 701            | Largest market, includes Hamptons suburbs |
| San Francisco | 186            | Includes broader Bay Area                 |
| Charleston    | 119            | Strong engagement per location            |
| Denver        | 78             | Includes Boulder metro                    |
| Los Angeles   | 63             | Growing market                            |

### Secondary Markets (5-50 Live Locations)

| Market         | Live Locations |
| -------------- | -------------- |
| Aspen          | 11             |
| Hamptons       | 9              |
| Boulder        | 9              |
| Colorado (ski) | 9              |
| Breckenridge   | 7              |
| Brooklyn       | 7              |
| Chicago        | 5              |

### Emerging Markets (<5 Live Locations)

Atlanta, Miami, Jersey City, Vail, West Palm Beach, Nashville, Hoboken, Montclair

---

## Query Patterns

### ⚠️ Important: Use `live = true` NOT `status = 'LIVE'`

The locations table uses a **boolean `live` column**, not a status text field.

```sql
-- CORRECT
WHERE l.live = true

-- WRONG (no status column exists)
WHERE l.status = 'LIVE'
```

---

### Live Locations by Market

```sql
SELECT
  n.city AS market,
  COUNT(DISTINCT l.location_id) AS live_locations
FROM locations l
JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
WHERE l.live = true
GROUP BY n.city
ORDER BY live_locations DESC
```

---

### Daily Check-ins by Market

```sql
SELECT
  n.city AS market,
  DATE(ci.created_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT ci.check_in_id) AS check_ins,
  COUNT(DISTINCT ci.user_id) AS unique_users
FROM check_ins ci
JOIN locations l ON l.location_id = ci.location_id
JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
WHERE l.live = true
  AND ci.created_at >= NOW() - INTERVAL '30 days'
GROUP BY 1, 2
ORDER BY 1, 2
```

---

### DAU by Market

```sql
SELECT
  n.city AS market,
  DATE(ci.created_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT ci.user_id) AS dau
FROM check_ins ci
JOIN locations l ON l.location_id = ci.location_id
JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
WHERE l.live = true
  AND DATE(ci.created_at AT TIME ZONE 'America/New_York') = CURRENT_DATE - 1
GROUP BY 1, 2
```

---

### TPV by Market

```sql
SELECT
  n.city AS market,
  DATE(c.paid_at AT TIME ZONE 'America/New_York') AS date,
  SUM(cs.check_share_total) / 100.0 AS tpv_dollars,
  COUNT(DISTINCT cs.user_id) AS paying_users
FROM check_shares cs
JOIN checks c ON c.check_id = cs.check_id
JOIN locations l ON l.location_id = c.location_id
JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
WHERE c.status = 'CLOSED'
  AND l.live = true
  AND c.paid_at >= NOW() - INTERVAL '30 days'
GROUP BY 1, 2
ORDER BY 1, 2
```

---

### Check-ins per Location by Market (Efficiency Metric)

```sql
SELECT
  n.city AS market,
  COUNT(DISTINCT l.location_id) AS live_locations,
  COUNT(DISTINCT ci.check_in_id) AS check_ins_l30d,
  ROUND(COUNT(DISTINCT ci.check_in_id)::numeric / COUNT(DISTINCT l.location_id), 1) AS checkins_per_location
FROM locations l
JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
LEFT JOIN check_ins ci ON ci.location_id = l.location_id
  AND ci.created_at >= NOW() - INTERVAL '30 days'
WHERE l.live = true
GROUP BY n.city
ORDER BY checkins_per_location DESC
```

---

### Neighborhood-Level Drill Down

```sql
SELECT
  n.city AS market,
  n.name AS neighborhood,
  COUNT(DISTINCT l.location_id) AS live_locations,
  COUNT(DISTINCT ci.check_in_id) AS check_ins_l30d
FROM locations l
JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
LEFT JOIN check_ins ci ON ci.location_id = l.location_id
  AND ci.created_at >= NOW() - INTERVAL '30 days'
WHERE l.live = true
  AND n.city = 'New York'  -- Filter to specific market
GROUP BY n.city, n.name
ORDER BY check_ins_l30d DESC
```

---

## Common Joins for Market Data

```
check_ins
    └── location_id → locations.location_id
                          └── neighborhood_id → neighborhoods.neighborhood_id
                                                    └── city (MARKET)

check_shares
    └── check_id → checks.check_id
                      └── location_id → locations.location_id
                                            └── neighborhood_id → neighborhoods.neighborhood_id
                                                                      └── city (MARKET)
```

---

## Time Zone Note

All daily metrics should use Eastern Time for consistency with org-wide KPIs:

```sql
AT TIME ZONE 'America/New_York'
```

---

## Data Quality Notes

1. **Duplicate city names**: Some cities have slight variations (e.g., "Los Angeles" vs "Los Angeles ", "Charleston" vs "Charleston, SC"). Consider normalizing with `TRIM()` or mapping.

2. **Brooklyn vs New York**: Brooklyn is sometimes listed separately from New York. May need to consolidate for true NYC market view.

3. **Ski markets**: Colorado, Breckenridge, Vail, Aspen are split - may want to group as "Colorado Ski" market.

---

## Suggested Market Groupings

```sql
CASE
  WHEN n.city IN ('New York', 'Brooklyn', 'Hamptons', 'Jersey City', 'Hoboken', 'White Plains') THEN 'NYC Metro'
  WHEN n.city IN ('San Francisco', ' San Francisco', 'Oakland', 'Sausalito', 'Marin', 'Berkeley') THEN 'SF Bay Area'
  WHEN n.city IN ('Denver', 'Boulder', 'Colorado', 'Aspen', 'Vail', 'Breckenridge', 'Breckenridge ') THEN 'Colorado'
  WHEN n.city IN ('Charleston', 'Charleston ', 'Charleston, SC') THEN 'Charleston'
  WHEN n.city IN ('Los Angeles', 'Los Angeles ') THEN 'Los Angeles'
  ELSE n.city
END AS market_group
```

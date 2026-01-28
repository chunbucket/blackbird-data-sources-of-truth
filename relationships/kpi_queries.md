# Daily Metrics KPI Dashboard - Query Reference

**Dashboard ID:** 3400
**Dashboard Name:** Daily Metrics - 1D
**Purpose:** Organization-wide KPI tracking

---

## Tables Used Across KPIs

| Table                         | Used In # KPIs | KPI Names                                                                                                                  |
| ----------------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `account_balances`            | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `account_transactions`        | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `activation_check_ins`        | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `activation_events`           | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `all_transactions`            | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `all_transactions_daily`      | 1              | TPV Yesterday vs Trailing 4wk Avg                                                                                          |
| `average_prior_weekdays`      | 1              | Check-Ins Yesterday vs Trailing 4wk Avg                                                                                    |
| `avg_by_dow`                  | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `avg_prior_4weekdays_dau`     | 1              | Unique DAU Yesterday vs Trailing 4wk Avg                                                                                   |
| `base`                        | 2              | Live Deals, Unique Paying Users Yesterday vs Trailing 4wk Avg                                                              |
| `check_in_counts`             | 2              | Check-ins / Live Location - Duplicate, Daily Check-ins / Live Location, 4wk                                                |
| `check_ins`                   | 6              | Check-ins / Live Location - Duplicate, Daily Check In Count, 4wk, Daily Unique DAU, 4wk...                                 |
| `check_ins_stacked`           | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `check_share_fly_redemptions` | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `check_share_payments`        | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `check_shares`                | 7              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `checkins_ranked`             | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `checks`                      | 2              | Daily Unique Paying Users 4wk, Unique Paying Users Yesterday vs Trailing 4wk Avg                                           |
| `city_zip_codes`              | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `city_zip_codes_agg`          | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `collab_card_renewals`        | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `collab_fly_redemptions`      | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `collab_purchases`            | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `collab_purchases_pre_fle`    | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `collaborations`              | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `collaborations_claimed`      | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `combined_user_activities`    | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `conversation_messages`       | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `counts`                      | 1              | Check-Ins Yesterday vs Trailing 4wk Avg                                                                                    |
| `coupon_card_swipes`          | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `coupon_fly_redemptions`      | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `created_at_day`              | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `d`                           | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `daily_downloads`             | 1              | Downloads Rolling 7D Avg                                                                                                   |
| `daily_metrics`               | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `daily_percentages`           | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `daily_totals`                | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `daily_tpv`                   | 1              | User Spend / Promotional Spend                                                                                             |
| `daily_with_dow`              | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `dau_by_date`                 | 1              | Unique DAU Yesterday vs Trailing 4wk Avg                                                                                   |
| `day_targets`                 | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `distinct_activation_events`  | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `downloads_by_date`           | 1              | Downloads Yesterday vs Trailing 4wk Avg                                                                                    |
| `final`                       | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `fly_ledger_entries`          | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `hubspot`                     | 1              | Signed Deals - Duplicate                                                                                                   |
| `location_summaries`          | 2              | Check-ins / Live Location - Duplicate, Daily Check-ins / Live Location, 4wk                                                |
| `locations`                   | 3              | Check-ins / Live Location - Duplicate, Daily Unique DAU, 4wk, Daily Check-ins / Live Location, 4wk                         |
| `memberships`                 | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `memberships_claimed`         | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `messages_sent`               | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `misc_payment_links`          | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `neighborhoods`               | 3              | Check-ins / Live Location - Duplicate, Daily Unique DAU, 4wk, Daily Check-ins / Live Location, 4wk                         |
| `nfc_chips`                   | 4              | Check-ins / Live Location - Duplicate, Daily Check In Count, 4wk, Daily Unique DAU, 4wk...                                 |
| `passes`                      | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `payment_links`               | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `payments`                    | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `pdr_deposit`                 | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `pdr_final_charge`            | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `prior_4weekdays`             | 2              | Unique DAU Yesterday vs Trailing 4wk Avg, Downloads Yesterday vs Trailing 4wk Avg                                          |
| `prior_4weekdays_dau`         | 1              | Unique DAU Yesterday vs Trailing 4wk Avg                                                                                   |
| `prior_4weekdays_tpv`         | 1              | TPV Yesterday vs Trailing 4wk Avg                                                                                          |
| `prior_avg`                   | 2              | Unique Paying Users Yesterday vs Trailing 4wk Avg, Downloads Yesterday vs Trailing 4wk Avg                                 |
| `prior_dates`                 | 1              | Unique Paying Users Yesterday vs Trailing 4wk Avg                                                                          |
| `prior_vals`                  | 2              | Unique Paying Users Yesterday vs Trailing 4wk Avg, Downloads Yesterday vs Trailing 4wk Avg                                 |
| `prior_weekdays`              | 2              | Check-Ins Yesterday vs Trailing 4wk Avg, TPV Yesterday vs Trailing 4wk Avg                                                 |
| `private_dining_rooms`        | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `referral_codes`              | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `referrals_sent`              | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `restaurants`                 | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `rolling_metrics`             | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `subscription_terms`          | 5              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `user_devices`                | 3              | Downloads Rolling 7D Avg, Daily Downloads, 4wk, Downloads Yesterday vs Trailing 4wk Avg                                    |
| `user_first_download`         | 3              | Downloads Rolling 7D Avg, Daily Downloads, 4wk, Downloads Yesterday vs Trailing 4wk Avg                                    |
| `user_tags`                   | 1              | Daily Unique DAU, 4wk                                                                                                      |
| `userpay`                     | 1              | User Spend / Promotional Spend                                                                                             |
| `users`                       | 8              | Tracking TPV to Goal, 281K, L7D TPV by Type, User Spend / Promotional Spend...                                             |
| `weekly_totals`               | 1              | Tracking TPV to Goal, 281K                                                                                                 |
| `with_rolling_avg`            | 1              | Downloads Rolling 7D Avg                                                                                                   |
| `yesterday`                   | 3              | Unique DAU Yesterday vs Trailing 4wk Avg, Check-Ins Yesterday vs Trailing 4wk Avg, Downloads Yesterday vs Trailing 4wk Avg |
| `yesterday_date`              | 1              | Unique Paying Users Yesterday vs Trailing 4wk Avg                                                                          |
| `yesterday_dau`               | 1              | Unique DAU Yesterday vs Trailing 4wk Avg                                                                                   |
| `yesterday_tpv`               | 1              | TPV Yesterday vs Trailing 4wk Avg                                                                                          |
| `yesterday_val`               | 2              | Unique Paying Users Yesterday vs Trailing 4wk Avg, Downloads Yesterday vs Trailing 4wk Avg                                 |

---

## KPI Queries

### Tracking TPV to Goal, 281K

**Card ID:** 10827
**Tables Used:** `account_balances, account_transactions, all_transactions, avg_by_dow, check_share_fly_redemptions, check_share_payments, check_shares, collab_card_renewals, collab_fly_redemptions, collab_purchases, collab_purchases_pre_fle, collaborations, coupon_card_swipes, coupon_fly_redemptions, created_at_day, d, daily_metrics, daily_percentages, daily_totals, daily_with_dow, day_targets, fly_ledger_entries, misc_payment_links, payment_links, payments, pdr_deposit, pdr_final_charge, private_dining_rooms, rolling_metrics, subscription_terms, users, weekly_totals`

```sql
WITH check_share_payments AS (
  SELECT
    'CHECK_SHARE' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    CAST(p.amount / 100.0 AS FLOAT) as adj_amount_usd,
    p.item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN check_shares cs ON fle.origin_id = cs.check_share_id
  WHERE p.status = 'SUCCEEDED'
    AND p.payment_method_id IS NOT NULL
    AND p.item_type IN ('CHECK_SHARE', 'FLY_AUTO_LOAD', 'CHECK')
    AND fle.origin_type = 'CHECK_SHARE'
    AND fle.credit_amount > 0
),

-- Direct collaboration purchases (not through FLE)
collab_purchases_pre_fle AS (
  SELECT
    'COLLAB - STRIPE/CHECKOUT' as transaction_type,
    p.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    p.amount / 100.0 as adj_amount_usd,
    p.item_id
  FROM payments p
  WHERE p.item_type = 'COLLAB'
    AND p.status = 'SUCCEEDED'
),

-- Check share FLY redemptions
check_share_fly_redemptions AS (
  SELECT
    'CHECK_SHARE_FLY_REDEMPTION' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    cs.user_id,
    fle.credit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM check_shares cs
  JOIN fly_ledger_entries fle ON fle.origin_id = cs.check_share_id
  WHERE fle.origin_type = 'CHECK_SHARE_REDEMPTION'
    AND fle.credit_amount > 0
),

-- Collaboration purchases through FLE
collab_purchases AS (
  SELECT
    'COLLAB' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^18 * 100.0) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id::text = u.user_id::text
  WHERE fle.origin_type = 'COLLAB'
    AND fle.debit_amount > 0
    AND ab.owner_type = 'USER'
    AND p.status = 'SUCCEEDED'
),

-- Collaboration FLY redemptions
collab_fly_redemptions AS (
  SELECT
    'COLLAB_FLY_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM account_transactions at
  JOIN collaborations c ON at.origin_id = c.collaboration_id
  JOIN fly_ledger_entries fle ON at.account_transaction_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE at.origin_type = 'COLLAB_REDEMPTION'
    AND fle.debit_amount > 0
),

-- Collaboration renewals
collab_card_renewals AS (
  SELECT
    'COLLAB_RENEWAL' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    p.amount / 100.0 as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM subscription_terms st
  JOIN fly_ledger_entries fle ON fle.origin_id = st.subscription_term_id
  JOIN payments p ON fle.account_transaction_id = p.item_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE fle.debit_amount > 0
    AND fle.origin_type IN ('SUBCRIPTION_TERM', 'SUBSCRIPTION_TERM')
    AND p.status = 'SUCCEEDED'
),

-- Coupon card swipes
coupon_card_swipes AS (
  SELECT
    'COUPON_CARD_SWIPE' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  JOIN payments p ON p.item_id = fle.account_transaction_id
  WHERE fle.origin_type = 'COUPON'
    AND p.status = 'SUCCEEDED'
    AND fle.debit_amount > 0
),

-- Coupon FLY redemptions
coupon_fly_redemptions AS (
  SELECT
    'COUPON_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  WHERE fle.origin_type = 'COUPON_REDEMPTION'
    AND fle.debit_amount > 0
),

pdr_final_charge AS (
   select 'PDR_FINAL_CHARGE' as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20) as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid as item_id
    from fly_ledger_entries
    join private_dining_rooms on private_dining_rooms.pdr_id = fly_ledger_entries.origin_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

pdr_deposit AS (
  select 'PDR_DEPOSIT'                                                 as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid               as item_id
    from fly_ledger_entries
    join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
    join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

misc_payment_links AS (
select 'MISC_PAYMENT_LINKS'                                                 as transaction_type,
               fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
               account_balances.account_balance_id,
               fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
               fly_ledger_entries.account_transaction_id::uuid               as item_id
        from fly_ledger_entries
        join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
        left join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
        join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
        where fly_ledger_entries.credit_amount > 0
        and private_dining_rooms.id is null -- NOT a private dining room
),

-- Combine all transaction types
all_transactions AS (
  SELECT * FROM check_share_payments
  UNION ALL
  SELECT * FROM check_share_fly_redemptions
  UNION ALL
  SELECT * FROM collab_purchases
  UNION ALL
  SELECT * FROM collab_purchases_pre_fle
  UNION ALL
  SELECT * FROM collab_fly_redemptions
  UNION ALL
  SELECT * FROM collab_card_renewals
  UNION ALL
  SELECT * FROM coupon_fly_redemptions
  UNION ALL
  SELECT * FROM coupon_card_swipes
  UNION ALL
  SELECT * FROM pdr_final_charge
  UNION ALL
  SELECT * FROM pdr_deposit
  UNION ALL
  SELECT * FROM misc_payment_links
)
,daily_totals AS (
  SELECT
    DATE_TRUNC('day', created_at_edt) AS created_at_day,
    SUM(adj_amount_usd) AS daily_tpv
  FROM all_transactions
  WHERE created_at_edt >= '2025-01-01'
    AND created_at_edt < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
  GROUP BY DATE_TRUNC('day', created_at_edt)
),

-- Add day of week and week grouping
daily_with_dow AS (
  SELECT
    created_at_day,
    daily_tpv,
    EXTRACT(DOW FROM created_at_day) AS day_of_week,
    TO_CHAR(created_at_day, 'Day') AS day_name,
    DATE_TRUNC('week', created_at_day) AS week_start
  FROM daily_totals
),

-- Calculate weekly totals
weekly_totals AS (
  SELECT
    week_start,
    SUM(daily_tpv) AS weekly_tpv
  FROM daily_with_dow
  GROUP BY week_start
),

-- Calculate percentage of week each day represents
daily_percentages AS (
  SELECT
    d.created_at_day,
    d.day_of_week,
    d.day_name,
    d.daily_tpv,
    w.weekly_tpv,
    (d.daily_tpv / w.weekly_tpv * 100) AS pct_of_week
  FROM daily_with_dow d
  JOIN weekly_totals w ON d.week_start = w.week_start
),

-- Calculate average percentage by day of week (this is each day's typical contribution to weekly total)
avg_by_dow AS (
  SELECT
    day_of_week,
    TRIM(day_name) AS day_name,
    AVG(pct_of_week) AS avg_pct_of_week,
    COUNT(*) AS num_weeks
  FROM daily_percentages
  GROUP BY day_of_week, day_name
),

-- Calculate target for each day based on 281K weekly average
-- Each day needs to contribute its historical percentage of the 281K * 7 weekly total
day_targets AS (
  SELECT
    day_of_week,
    day_name,
    avg_pct_of_week,
    -- 281K daily average * 7 days = 1,967K weekly total
    -- Each day should contribute its percentage of that
    (1967000 * avg_pct_of_week / 100) AS target_tpv_for_day
  FROM avg_by_dow
),

-- Calculate daily metrics with progress toward target
daily_metrics AS (
  SELECT
    d.created_at_day,
    TRIM(TO_CHAR(d.created_at_day, 'Day')) AS day_name,
    d.daily_tpv AS actual_tpv,
    t.target_tpv_for_day,
    t.avg_pct_of_week AS historical_pct_contribution,
    -- Progress toward that day's contribution to 281K average
    (d.daily_tpv / t.target_tpv_for_day * 100) AS pct_of_target,
    -- Implied weekly average if all days performed like today
    (d.daily_tpv / t.avg_pct_of_week * 100 / 7) AS implied_daily_avg
  FROM daily_totals d
  JOIN day_targets t ON EXTRACT(DOW FROM d.created_at_day) = t.day_of_week
),

-- Add rolling averages of implied daily average
rolling_metrics AS (
  SELECT
    created_at_day,
    day_name,
    actual_tpv,
    target_tpv_for_day,
    historical_pct_contribution,
    pct_of_target,
    implied_daily_avg,
    -- 7-day rolling average of implied daily average
    AVG(implied_daily_avg) OVER (
      ORDER BY created_at_day
      ROWS BETWEEN 6 PRECEDING AND CURRENT ROW
    ) AS rolling_7d_avg,
    -- Count how many days in the rolling window (important for first week)
    COUNT(*) OVER (
      ORDER BY created_at_day
      ROWS BETWEEN 6 PRECEDING AND CURRENT ROW
    ) AS days_in_window
  FROM daily_metrics
)

-- Final output with milestone tracking
SELECT
  created_at_day,
  day_name,
  ROUND(actual_tpv::numeric, 0) AS actual_tpv,
  ROUND(target_tpv_for_day::numeric, 0) AS day_target,
  ROUND(historical_pct_contribution::numeric, 1) || '%' AS typical_week_contribution,
  ROUND(pct_of_target::numeric, 1) || '%' AS pct_of_day_target,
  ROUND(implied_daily_avg::numeric, 0) AS implied_avg,
  ROUND(rolling_7d_avg::numeric, 0) AS rolling_7d_avg,
  ROUND((rolling_7d_avg / 281000 * 100)::numeric, 1) AS pct_to_281k_avg,
  -- Progress indicators based on rolling average
  CASE
    WHEN rolling_7d_avg >= 280000 THEN '👑 280k+ Avg! (99.6%+)'
    WHEN rolling_7d_avg >= 270000 THEN '🏆 270k+ Avg! (96%+)'
    WHEN rolling_7d_avg >= 260000 THEN '💎 260k+ Avg! (93%+)'
    WHEN rolling_7d_avg >= 250000 THEN '🎯 250k+ Avg! (89%+)'
    WHEN rolling_7d_avg >= 240000 THEN '🔥 240k+ Avg! (85%+)'
    WHEN rolling_7d_avg >= 230000 THEN '⚡ 230k+ Avg! (82%+)'
    WHEN rolling_7d_avg >= 220000 THEN '💫 220k+ Avg! (78%+)'
    WHEN rolling_7d_avg >= 210000 THEN '📈 210k+ Avg! (75%+)'
    WHEN rolling_7d_avg >= 200000 THEN '💪 200k+ Avg! (71%+)'
    WHEN rolling_7d_avg >= 190000 THEN '🚀 190k+ Avg! (68%+)'
    WHEN rolling_7d_avg >= 180000 THEN '🌟 180k+ Avg! (64%+)'
    WHEN rolling_7d_avg >= 170000 THEN '✨ 170k+ Avg! (60%+)'
    WHEN rolling_7d_avg >= 160000 THEN '🎪 160k+ Avg! (57%+)'
    WHEN rolling_7d_avg >= 150000 THEN '🎨 150k+ Avg! (53%+)'
    WHEN rolling_7d_avg >= 140000 THEN '🌈 140k+ Avg! (50%+)'
    WHEN rolling_7d_avg >= 130000 THEN '🎭 130k+ Avg! (46%+)'
    WHEN rolling_7d_avg >= 120000 THEN '🎸 120k+ Avg! (43%+)'
    WHEN rolling_7d_avg >= 110000 THEN '🎯 110k+ Avg! (39%+)'
    WHEN rolling_7d_avg >= 100000 THEN '🏅 100k+ Avg! (36%+)'
    WHEN rolling_7d_avg >= 90000 THEN '🌺 90k+ Avg! (32%+)'
    WHEN rolling_7d_avg >= 80000 THEN '🌻 80k+ Avg! (28%+)'
    WHEN rolling_7d_avg >= 70000 THEN '🌷 70k+ Avg! (25%+)'
    WHEN rolling_7d_avg >= 60000 THEN '🌿 60k+ Avg! (21%+)'
    WHEN rolling_7d_avg >= 50000 THEN '🌱 50k+ Avg! (18%+)'
    WHEN rolling_7d_avg >= 40000 THEN '🌾 40k+ Avg! (14%+)'
    WHEN rolling_7d_avg >= 30000 THEN '🌸 30k+ Avg! (11%+)'
    WHEN rolling_7d_avg >= 20000 THEN '🌼 20k+ Avg! (7%+)'
    ELSE '🌱 Building momentum'
  END AS milestone_status,
  -- Gap to next milestone
  CASE
    WHEN rolling_7d_avg >= 280000 THEN 281000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 270000 THEN 280000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 260000 THEN 270000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 250000 THEN 260000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 240000 THEN 250000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 230000 THEN 240000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 220000 THEN 230000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 210000 THEN 220000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 200000 THEN 210000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 190000 THEN 200000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 180000 THEN 190000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 170000 THEN 180000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 160000 THEN 170000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 150000 THEN 160000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 140000 THEN 150000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 130000 THEN 140000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 120000 THEN 130000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 110000 THEN 120000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 100000 THEN 110000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 90000 THEN 100000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 80000 THEN 90000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 70000 THEN 80000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 60000 THEN 70000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 50000 THEN 60000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 40000 THEN 50000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 30000 THEN 40000 - rolling_7d_avg
    WHEN rolling_7d_avg >= 20000 THEN 30000 - rolling_7d_avg
    ELSE 20000 - rolling_7d_avg
  END AS avg_gap_to_next_milestone,
  -- Show if today is better or worse than its specific target
  CASE
    WHEN pct_of_target > 100 THEN '📊 Above target (' || ROUND((pct_of_target - 100)::numeric, 1) || '% over)'
    WHEN pct_of_target < 100 THEN '📉 Below target (' || ROUND((100 - pct_of_target)::numeric, 1) || '% under)'
    ELSE '📊 On target'
  END AS daily_performance
FROM rolling_metrics
WHERE days_in_window >= 4  -- Only show once we have at least 4 days of data
AND created_at_day >= '2025-07-01'
ORDER BY created_at_day ASC;
```

---

### L7D TPV by Type

**Card ID:** 19174
**Tables Used:** `account_balances, account_transactions, all_transactions, check_share_fly_redemptions, check_share_payments, check_shares, collab_card_renewals, collab_fly_redemptions, collab_purchases, collab_purchases_pre_fle, collaborations, coupon_card_swipes, coupon_fly_redemptions, fly_ledger_entries, misc_payment_links, payment_links, payments, pdr_deposit, pdr_final_charge, private_dining_rooms, subscription_terms, users`

```sql
WITH check_share_payments AS (
  SELECT
    'CHECK_SHARE' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    CAST(p.amount / 100.0 AS FLOAT) as adj_amount_usd,
    p.item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN check_shares cs ON fle.origin_id = cs.check_share_id
  WHERE p.status = 'SUCCEEDED'
    AND p.payment_method_id IS NOT NULL
    AND p.item_type IN ('CHECK_SHARE', 'FLY_AUTO_LOAD', 'CHECK')
    AND fle.origin_type = 'CHECK_SHARE'
    AND fle.credit_amount > 0
),

-- Direct collaboration purchases (not through FLE)
collab_purchases_pre_fle AS (
  SELECT
    'COLLAB - STRIPE/CHECKOUT' as transaction_type,
    p.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    p.amount / 100.0 as adj_amount_usd,
    p.item_id
  FROM payments p
  WHERE p.item_type = 'COLLAB'
    AND p.status = 'SUCCEEDED'
),

-- Check share FLY redemptions
check_share_fly_redemptions AS (
  SELECT
    'CHECK_SHARE_FLY_REDEMPTION' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    cs.user_id,
    fle.credit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM check_shares cs
  JOIN fly_ledger_entries fle ON fle.origin_id = cs.check_share_id
  WHERE fle.origin_type = 'CHECK_SHARE_REDEMPTION'
    AND fle.credit_amount > 0
),

-- Collaboration purchases through FLE
collab_purchases AS (
  SELECT
    'COLLAB' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^18 * 100.0) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id::text = u.user_id::text
  WHERE fle.origin_type = 'COLLAB'
    AND fle.debit_amount > 0
    AND ab.owner_type = 'USER'
    AND p.status = 'SUCCEEDED'
),

-- Collaboration FLY redemptions
collab_fly_redemptions AS (
  SELECT
    'COLLAB_FLY_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM account_transactions at
  JOIN collaborations c ON at.origin_id = c.collaboration_id
  JOIN fly_ledger_entries fle ON at.account_transaction_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE at.origin_type = 'COLLAB_REDEMPTION'
    AND fle.debit_amount > 0
),

-- Collaboration renewals
collab_card_renewals AS (
  SELECT
    'COLLAB_RENEWAL' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    p.amount / 100.0 as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM subscription_terms st
  JOIN fly_ledger_entries fle ON fle.origin_id = st.subscription_term_id
  JOIN payments p ON fle.account_transaction_id = p.item_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE fle.debit_amount > 0
    AND fle.origin_type IN ('SUBCRIPTION_TERM', 'SUBSCRIPTION_TERM')
    AND p.status = 'SUCCEEDED'
),

-- Coupon card swipes
coupon_card_swipes AS (
  SELECT
    'COUPON_CARD_SWIPE' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  JOIN payments p ON p.item_id = fle.account_transaction_id
  WHERE fle.origin_type = 'COUPON'
    AND p.status = 'SUCCEEDED'
    AND fle.debit_amount > 0
),

-- Coupon FLY redemptions
coupon_fly_redemptions AS (
  SELECT
    'COUPON_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  WHERE fle.origin_type = 'COUPON_REDEMPTION'
    AND fle.debit_amount > 0
),

pdr_final_charge AS (
   select 'PDR_FINAL_CHARGE' as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20) as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid as item_id
    from fly_ledger_entries
    join private_dining_rooms on private_dining_rooms.pdr_id = fly_ledger_entries.origin_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

pdr_deposit AS (
  select 'PDR_DEPOSIT'                                                 as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid               as item_id
    from fly_ledger_entries
    join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
    join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

misc_payment_links AS (
select 'MISC_PAYMENT_LINKS'                                                 as transaction_type,
               fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
               account_balances.account_balance_id,
               fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
               fly_ledger_entries.account_transaction_id::uuid               as item_id
        from fly_ledger_entries
        join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
        left join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
        join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
        where fly_ledger_entries.credit_amount > 0
        and private_dining_rooms.id is null -- NOT a private dining room
),

-- Combine all transaction types
all_transactions AS (
  SELECT * FROM check_share_payments
  UNION ALL
  SELECT * FROM check_share_fly_redemptions
  UNION ALL
  SELECT * FROM collab_purchases
  UNION ALL
  SELECT * FROM collab_purchases_pre_fle
  UNION ALL
  SELECT * FROM collab_fly_redemptions
  UNION ALL
  SELECT * FROM collab_card_renewals
  UNION ALL
  SELECT * FROM coupon_fly_redemptions
  UNION ALL
  SELECT * FROM coupon_card_swipes
  UNION ALL
  SELECT * FROM pdr_final_charge
  UNION ALL
  SELECT * FROM pdr_deposit
  UNION ALL
  SELECT * FROM misc_payment_links

)

-- Group by day only (matching original output)
SELECT
  DATE_TRUNC('day', created_at_edt) AS created_at_day,
  transaction_type, --CASE WHEN transaction_type IN ('PDR_DEPOSIT','PDR_FINAL_CHARGE','MISC_PAYMENT_LINKS') THEN 'PDR' ELSE transaction_type end as t_type,
  --user_id,
  --item_id,
  SUM(adj_amount_usd) AS tpv
FROM all_transactions
WHERE TRUE
--AND created_at_edt >= '2025-11-01'
AND created_at_edt >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '8 days') AS date))::timestamptz
AND created_at_edt < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
GROUP BY 1,2
ORDER BY 1 DESC

```

---

### Downloads Rolling 7D Avg

**Card ID:** 19373
**Tables Used:** `daily_downloads, user_devices, user_first_download, with_rolling_avg`

```sql
WITH daily_downloads AS (
  SELECT
    CAST("source"."time_first_downloaded_est" AS date) AS "date_first_downloaded_est",
    COUNT(*) AS "count"
  FROM
    (
      WITH user_first_download AS (
        SELECT
          user_id,
          MIN(
            created_at AT TIME ZONE 'America/New_York'
          ) AS time_first_downloaded_est,
          'ios' as type
        FROM
          user_devices
        WHERE
          lower(user_agent) LIKE '%darwin%'
          AND lower(user_agent) NOT LIKE '%clip%'
        GROUP BY
          user_id
        UNION ALL
        SELECT
          user_id,
          MIN(
            created_at AT TIME ZONE 'America/New_York'
          ) AS time_first_downloaded_est,
          'android' as type
        FROM
          user_devices
        WHERE
          lower(user_agent) LIKE '%android%'
          AND lower(user_agent) NOT LIKE '%clip%'
        GROUP BY
          user_id
      )
      SELECT
        *
      FROM
        user_first_download
    ) AS "source"
  WHERE
    "source"."time_first_downloaded_est" >= (NOW() AT TIME ZONE 'America/New_York' - INTERVAL '5 weeks')
    AND "source"."time_first_downloaded_est" < CAST((NOW() AT TIME ZONE 'America/New_York') AS date)
  GROUP BY
    CAST("source"."time_first_downloaded_est" AS date)
),
with_rolling_avg AS (
  SELECT
    date_first_downloaded_est,
    count,
    AVG(count) OVER (
      ORDER BY date_first_downloaded_est
      ROWS BETWEEN 6 PRECEDING AND CURRENT ROW
    ) AS rolling_7d_avg,
    COUNT(*) OVER (
      ORDER BY date_first_downloaded_est
      ROWS BETWEEN 6 PRECEDING AND CURRENT ROW
    ) AS days_in_window
  FROM
    daily_downloads
)
SELECT
  date_first_downloaded_est,
  count,
  rolling_7d_avg
FROM
  with_rolling_avg
WHERE
  date_first_downloaded_est >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '5 weeks') AS date))
  AND days_in_window >= 7  -- Only show when we have a full 7 days
ORDER BY
  date_first_downloaded_est ASC
```

---

### User Spend / Promotional Spend

**Card ID:** 19570
**Tables Used:** `account_balances, account_transactions, all_transactions, check_share_fly_redemptions, check_share_payments, check_shares, collab_card_renewals, collab_fly_redemptions, collab_purchases, collab_purchases_pre_fle, collaborations, coupon_card_swipes, coupon_fly_redemptions, daily_tpv, fly_ledger_entries, misc_payment_links, payment_links, payments, pdr_deposit, pdr_final_charge, private_dining_rooms, subscription_terms, userpay, users`

```sql
WITH check_share_payments AS (
  SELECT
    'CHECK_SHARE' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    CAST(p.amount / 100.0 AS FLOAT) as adj_amount_usd,
    p.item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN check_shares cs ON fle.origin_id = cs.check_share_id
  WHERE p.status = 'SUCCEEDED'
    AND p.payment_method_id IS NOT NULL
    AND p.item_type IN ('CHECK_SHARE', 'FLY_AUTO_LOAD', 'CHECK')
    AND fle.origin_type = 'CHECK_SHARE'
    AND fle.credit_amount > 0
),

-- Direct collaboration purchases (not through FLE)
collab_purchases_pre_fle AS (
  SELECT
    'COLLAB - STRIPE/CHECKOUT' as transaction_type,
    p.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    p.amount / 100.0 as adj_amount_usd,
    p.item_id
  FROM payments p
  WHERE p.item_type = 'COLLAB'
    AND p.status = 'SUCCEEDED'
),

-- Check share FLY redemptions
check_share_fly_redemptions AS (
  SELECT
    'CHECK_SHARE_FLY_REDEMPTION' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    cs.user_id,
    fle.credit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM check_shares cs
  JOIN fly_ledger_entries fle ON fle.origin_id = cs.check_share_id
  WHERE fle.origin_type = 'CHECK_SHARE_REDEMPTION'
    AND fle.credit_amount > 0
),

-- Collaboration purchases through FLE
collab_purchases AS (
  SELECT
    'COLLAB' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^18 * 100.0) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id::text = u.user_id::text
  WHERE fle.origin_type = 'COLLAB'
    AND fle.debit_amount > 0
    AND ab.owner_type = 'USER'
    AND p.status = 'SUCCEEDED'
),

-- Collaboration FLY redemptions
collab_fly_redemptions AS (
  SELECT
    'COLLAB_FLY_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM account_transactions at
  JOIN collaborations c ON at.origin_id = c.collaboration_id
  JOIN fly_ledger_entries fle ON at.account_transaction_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE at.origin_type = 'COLLAB_REDEMPTION'
    AND fle.debit_amount > 0
),

-- Collaboration renewals
collab_card_renewals AS (
  SELECT
    'COLLAB_RENEWAL' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    p.amount / 100.0 as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM subscription_terms st
  JOIN fly_ledger_entries fle ON fle.origin_id = st.subscription_term_id
  JOIN payments p ON fle.account_transaction_id = p.item_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE fle.debit_amount > 0
    AND fle.origin_type IN ('SUBCRIPTION_TERM', 'SUBSCRIPTION_TERM')
    AND p.status = 'SUCCEEDED'
),

-- Coupon card swipes
coupon_card_swipes AS (
  SELECT
    'COUPON_CARD_SWIPE' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  JOIN payments p ON p.item_id = fle.account_transaction_id
  WHERE fle.origin_type = 'COUPON'
    AND p.status = 'SUCCEEDED'
    AND fle.debit_amount > 0
),

-- Coupon FLY redemptions
coupon_fly_redemptions AS (
  SELECT
    'COUPON_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  WHERE fle.origin_type = 'COUPON_REDEMPTION'
    AND fle.debit_amount > 0
),

pdr_final_charge AS (
   select 'PDR_FINAL_CHARGE' as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20) as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid as item_id
    from fly_ledger_entries
    join private_dining_rooms on private_dining_rooms.pdr_id = fly_ledger_entries.origin_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

pdr_deposit AS (
  select 'PDR_DEPOSIT'                                                 as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid               as item_id
    from fly_ledger_entries
    join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
    join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

misc_payment_links AS (
select 'MISC_PAYMENT_LINKS'                                                 as transaction_type,
               fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
               account_balances.account_balance_id,
               fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
               fly_ledger_entries.account_transaction_id::uuid               as item_id
        from fly_ledger_entries
        join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
        left join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
        join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
        where fly_ledger_entries.credit_amount > 0
        and private_dining_rooms.id is null -- NOT a private dining room
),

-- Combine all transaction types
all_transactions AS (
  SELECT * FROM check_share_payments
  UNION ALL
  SELECT * FROM check_share_fly_redemptions
  UNION ALL
  SELECT * FROM collab_purchases
  UNION ALL
  SELECT * FROM collab_purchases_pre_fle
  UNION ALL
  SELECT * FROM collab_fly_redemptions
  UNION ALL
  SELECT * FROM collab_card_renewals
  UNION ALL
  SELECT * FROM coupon_fly_redemptions
  UNION ALL
  SELECT * FROM coupon_card_swipes
  UNION ALL
  SELECT * FROM pdr_final_charge
  UNION ALL
  SELECT * FROM pdr_deposit
  UNION ALL
  SELECT * FROM misc_payment_links

),

userpay as (
  select mo, sum(amt) as amt
  from (
      select date_trunc('day', created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC') as mo, sum(amount) / 1e2 amt
      from payments
      where payments.status = 'SUCCEEDED'
      group by 1

      union

      select date_trunc('day', created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC') mo, sum(credit_amount / 1e18) / 1e2 amt
      from fly_ledger_entries
      where fly_ledger_entries.origin_type = 'USDC_TO_FLY'
      group by 1
  ) _
  where mo >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '31 day') AS date))::timestamptz
  AND mo < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
  group by mo
),

daily_tpv AS (
  SELECT
    DATE_TRUNC('day', created_at_edt) AS created_at_day,
    SUM(adj_amount_usd) AS total_tpv
  FROM all_transactions
  WHERE created_at_edt >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '31 day') AS date))::timestamptz
  AND created_at_edt < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
  GROUP BY 1
)

-- Final output with user_spend and promotional_spend
SELECT
  dt.created_at_day,
  'user_spend' as tpv_type,
  COALESCE(up.amt, 0) as tpv
FROM daily_tpv dt
LEFT JOIN userpay up ON dt.created_at_day = up.mo

UNION ALL

SELECT
  dt.created_at_day,
  'promotional_spend' as tpv_type,
  dt.total_tpv - COALESCE(up.amt, 0) as tpv
FROM daily_tpv dt
LEFT JOIN userpay up ON dt.created_at_day = up.mo

ORDER BY created_at_day DESC, tpv_type;
```

---

### Check-ins / Live Location - Duplicate

**Card ID:** 7328
**Description:** Consumer check-ins per # locations live on a given day. This does NOT include employee check ins on the purple pucks.
**Tables Used:** `check_in_counts, check_ins, location_summaries, locations, neighborhoods, nfc_chips`

```sql
WITH
  check_in_counts AS (
    SELECT
      DATE(ci.created_at AT TIME ZONE 'America/New_York') AS date,
      n.neighborhood_id,
      COUNT(DISTINCT check_in_id) AS check_in_count
    FROM
      check_ins ci
      JOIN locations l ON l.location_id = ci.location_id
      JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
      LEFT JOIN nfc_chips nfc ON nfc.nfc_chip_id = ci.nfc_chip_id
    WHERE
      DATE(ci.created_at AT TIME ZONE 'America/New_York') >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))
      AND DATE(ci.created_at AT TIME ZONE 'America/New_York') < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))
      --AND nfc.action <> 'EMPLOYEE_CHECK_IN'
    GROUP BY 1,2
  )
SELECT
  DATE(ls.date AT TIME ZONE 'America/New_York') as date_est,
  -- ls.neighborhood_id,
  SUM(ls.live) as total_live,
  SUM(ls.payments_enabled) as total_payments_enabled,
  COALESCE(SUM(cic.check_in_count), 0) as total_check_ins,
  CASE
        WHEN COALESCE(SUM(ls.live), 0) > 0
        THEN ROUND(COALESCE(SUM(cic.check_in_count), 0) * 1.0 / COALESCE(SUM(ls.live), 0), 2)
        ELSE 0
    END AS avg_check_ins_per_live_location
FROM
  location_summaries ls
  LEFT JOIN check_in_counts cic
    ON cic.neighborhood_id = ls.neighborhood_id
   AND ls.date = cic.date
WHERE
  DATE(ls.date AT TIME ZONE 'America/New_York') >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))
  AND DATE(ls.date AT TIME ZONE 'America/New_York') < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))
GROUP BY 1

```

---

### Signed Deals - Duplicate

**Card ID:** 7342
**Tables Used:** `hubspot`

```sql
SELECT
    COUNT(*) FILTER (WHERE deal_stage IN ('ready', 'kickoff', 'seeding', 'install', 'live', 'stalledblocked')) AS signed_count
FROM hubspot.deals
WHERE pass_sale_type IS NULL
   OR strpos(lower(trim(pass_sale_type)), 'just add to pass') = 0;
```

---

### Live Deals

**Card ID:** 7343
**Tables Used:** `base`

```sql
-- total live
WITH base AS (
    SELECT
        DISTINCT CONCAT(aa.restaurant_name,'-',aa.location_name,'-',aa.restaurant_id) AS location_distinct,
        aa.deal_stage,
        aa.pass_sale_type
    FROM {{#13102-hubspot-sync-w-database-model}} aa
    WHERE deal_stage = 'live'
      AND deal_name NOT ILIKE '%Breakfast Club%'
)

SELECT
    COUNT(*) FILTER (WHERE deal_stage = 'live') AS number_of_locations
FROM base;

```

---

### TPV: Daily, 4wk

**Card ID:** 7832
**Description:** From [🐦‍⬛ CORE] [TODAY, TOTAL SUM] New TPV: Check Shares Card Swipes, Check Shares FLY Redeemed, Collabs Card Swipes, Collabs FLY Redeemed - Duplicate - Modified
**Tables Used:** `account_balances, account_transactions, all_transactions, check_share_fly_redemptions, check_share_payments, check_shares, collab_card_renewals, collab_fly_redemptions, collab_purchases, collab_purchases_pre_fle, collaborations, coupon_card_swipes, coupon_fly_redemptions, fly_ledger_entries, misc_payment_links, payment_links, payments, pdr_deposit, pdr_final_charge, private_dining_rooms, subscription_terms, users`

```sql
WITH check_share_payments AS (
  SELECT
    'CHECK_SHARE' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    CAST(p.amount / 100.0 AS FLOAT) as adj_amount_usd,
    p.item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN check_shares cs ON fle.origin_id = cs.check_share_id
  WHERE p.status = 'SUCCEEDED'
    AND p.payment_method_id IS NOT NULL
    AND p.item_type IN ('CHECK_SHARE', 'FLY_AUTO_LOAD', 'CHECK')
    AND fle.origin_type = 'CHECK_SHARE'
    AND fle.credit_amount > 0
),

-- Direct collaboration purchases (not through FLE)
collab_purchases_pre_fle AS (
  SELECT
    'COLLAB - STRIPE/CHECKOUT' as transaction_type,
    p.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    p.amount / 100.0 as adj_amount_usd,
    p.item_id
  FROM payments p
  WHERE p.item_type = 'COLLAB'
    AND p.status = 'SUCCEEDED'
),

-- Check share FLY redemptions
check_share_fly_redemptions AS (
  SELECT
    'CHECK_SHARE_FLY_REDEMPTION' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    cs.user_id,
    fle.credit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM check_shares cs
  JOIN fly_ledger_entries fle ON fle.origin_id = cs.check_share_id
  WHERE fle.origin_type = 'CHECK_SHARE_REDEMPTION'
    AND fle.credit_amount > 0
),

-- Collaboration purchases through FLE
collab_purchases AS (
  SELECT
    'COLLAB' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^18 * 100.0) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id::text = u.user_id::text
  WHERE fle.origin_type = 'COLLAB'
    AND fle.debit_amount > 0
    AND ab.owner_type = 'USER'
    AND p.status = 'SUCCEEDED'
),

-- Collaboration FLY redemptions
collab_fly_redemptions AS (
  SELECT
    'COLLAB_FLY_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM account_transactions at
  JOIN collaborations c ON at.origin_id = c.collaboration_id
  JOIN fly_ledger_entries fle ON at.account_transaction_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE at.origin_type = 'COLLAB_REDEMPTION'
    AND fle.debit_amount > 0
),

-- Collaboration renewals
collab_card_renewals AS (
  SELECT
    'COLLAB_RENEWAL' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    p.amount / 100.0 as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM subscription_terms st
  JOIN fly_ledger_entries fle ON fle.origin_id = st.subscription_term_id
  JOIN payments p ON fle.account_transaction_id = p.item_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE fle.debit_amount > 0
    AND fle.origin_type IN ('SUBCRIPTION_TERM', 'SUBSCRIPTION_TERM')
    AND p.status = 'SUCCEEDED'
),

-- Coupon card swipes
coupon_card_swipes AS (
  SELECT
    'COUPON_CARD_SWIPE' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  JOIN payments p ON p.item_id = fle.account_transaction_id
  WHERE fle.origin_type = 'COUPON'
    AND p.status = 'SUCCEEDED'
    AND fle.debit_amount > 0
),

-- Coupon FLY redemptions
coupon_fly_redemptions AS (
  SELECT
    'COUPON_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  WHERE fle.origin_type = 'COUPON_REDEMPTION'
    AND fle.debit_amount > 0
),

pdr_final_charge AS (
   select 'PDR_FINAL_CHARGE' as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20) as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid as item_id
    from fly_ledger_entries
    join private_dining_rooms on private_dining_rooms.pdr_id = fly_ledger_entries.origin_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

pdr_deposit AS (
  select 'PDR_DEPOSIT'                                                 as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid               as item_id
    from fly_ledger_entries
    join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
    join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

misc_payment_links AS (
select 'MISC_PAYMENT_LINKS'                                                 as transaction_type,
               fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
               account_balances.account_balance_id,
               fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
               fly_ledger_entries.account_transaction_id::uuid               as item_id
        from fly_ledger_entries
        join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
        left join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
        join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
        where fly_ledger_entries.credit_amount > 0
        and private_dining_rooms.id is null -- NOT a private dining room
),

-- Combine all transaction types
all_transactions AS (
  SELECT * FROM check_share_payments
  UNION ALL
  SELECT * FROM check_share_fly_redemptions
  UNION ALL
  SELECT * FROM collab_purchases
  UNION ALL
  SELECT * FROM collab_purchases_pre_fle
  UNION ALL
  SELECT * FROM collab_fly_redemptions
  UNION ALL
  SELECT * FROM collab_card_renewals
  UNION ALL
  SELECT * FROM coupon_fly_redemptions
  UNION ALL
  SELECT * FROM coupon_card_swipes
  UNION ALL
  SELECT * FROM pdr_final_charge
  UNION ALL
  SELECT * FROM pdr_deposit
  UNION ALL
  SELECT * FROM misc_payment_links

)

-- Group by day only (matching original output)
SELECT
  DATE_TRUNC('day', created_at_edt) AS created_at_day,
  transaction_type,
  --user_id,
  --item_id,
  SUM(adj_amount_usd) AS tpv
FROM all_transactions
WHERE created_at_edt >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))::timestamptz
AND created_at_edt < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
GROUP BY 1,2
ORDER BY 1 DESC

```

---

### Daily Check In Count, 4wk

**Card ID:** 7834
**Description:** Shows the count of check ins, grouped by how they were initiated. This DOES include employee check ins on the purple pucks.

NFC
URL - via joining a check
GPS
RESERVATION - via reservation notifcation
BEACON
**Tables Used:** `check_ins, nfc_chips`

```sql
--ALL CHECKINS REGARDLESS OF RESTAURANT STATUS, OR EMPLOYEE vs GUEST
SELECT
  DATE (check_ins.created_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT check_in_id) as check_ins
FROM check_ins
  LEFT JOIN nfc_chips ON nfc_chips.nfc_chip_id = check_ins.nfc_chip_id
WHERE
  DATE (check_ins.created_at AT TIME ZONE 'America/New_York')
  BETWEEN DATE ((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '29 days')
  AND DATE ((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '1 day')
GROUP BY
  1
ORDER BY
  1 DESC
```

---

### Daily Unique DAU, 4wk

**Card ID:** 7835
**Description:** From [🐦‍⬛ CORE KPI] DAU, Today - Duplicate - Modified
**Tables Used:** `activation_check_ins, activation_events, check_ins, check_ins_stacked, checkins_ranked, city_zip_codes, city_zip_codes_agg, collaborations_claimed, combined_user_activities, conversation_messages, distinct_activation_events, final, locations, memberships, memberships_claimed, messages_sent, neighborhoods, nfc_chips, passes, referral_codes, referrals_sent, restaurants, user_tags, users`

```sql
SELECT
  CAST("source"."created_at_edt" AS date) AS "created_at_edt",
  count(distinct "source"."user_id") AS "count"
FROM
  (
    with referrals_sent as (
      SELECT
        created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
        user_id :: text,
        referral_codes.code :: text as activity_id,
        'REFERRAL' as activity_type
      from
        referral_codes
    ),
    messages_sent as (
      SELECT
        conversation_messages.timestamp AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
        author :: text as user_id,
        conversation_id :: text as activity_id,
        'MESSAGE SENT' as activity_type
      from
        conversation_messages
      where
        author_type = 'USER'
    ),
    memberships_claimed as (
      SELECT
        created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
        user_id :: text,
        memberships.membership_id :: text as activity_id,
        'MEMBERSHIP' as activity_type
      from
        memberships
    ),
    collaborations_claimed as (
      SELECT
        created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
        user_id :: text,
        passes.pass_id :: text as activity_id,
        'COLLABORATION_CLAIMED' as activity_type
      from
        passes
    ),
    check_ins_stacked as (
      select
        created_at_edt,
        user_id :: text,
        check_in_id :: text as activity_id,
        CASE
          WHEN check_in_type = 'repeat_check_in' then 'REPEAT_CHECK_IN'
          WHEN check_in_type = 'new_check_in' then 'NEW_CHECK_IN'
        END as activity_type
      from
        (
          with distinct_activation_events as (
            SELECT
              *
            FROM
              (
                SELECT
                  activation_event_id,
                  description,
                  location_id,
                  start_date,
                  end_date,
                  ROW_NUMBER() OVER (
                    PARTITION BY location_id,
                    start_date,
                    end_date

ORDER BY
                      activation_event_id
                  ) AS row_num
                FROM
                  activation_events
              ) a

WHERE
              row_num = 1
          ),
          activation_check_ins as (
            select
              distinct check_in_id,
              array_agg(dae.description) as all_activation_descriptions,
              array_agg(dae.activation_event_id) as all_activation_event_ids,
              count(dae.activation_event_id) as num_activations_tagged
            from
              check_ins
              inner join distinct_activation_events dae on check_ins.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' >= dae.start_date

   AND check_ins.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' < dae.end_date
              AND check_ins.location_id = dae.location_id
            group by
              check_in_id
          ),
          checkins_ranked as (
            select
              *,
              row_number() over (
                partition by user_id
                order by
                  created_at asc
              ) as rnk
            from
              check_ins
          ),
          city_zip_codes_agg as (
            select
              city_zip_codes.zip_code,
              array_agg(region) as city_zip_codes_regions
            from
              city_zip_codes
            group by
              (city_zip_codes.zip_code)
          ),
          final as (
            select
              distinct checkins_ranked.*,
              CASE
                WHEN checkins_ranked.rnk = 1 THEN 'new_check_in'
                ELSE 'repeat_check_in'
              END as check_in_type,
              checkins_ranked.created_at at time zone 'america/new_york' at time zone 'utc' as created_at_edt,
              checkins_ranked.created_at at time zone locations.time_zone at time zone 'utc' as created_at_local_time,
              date(
                checkins_ranked.created_at at time zone 'america/new_york' at time zone 'utc'
              ) as date_edt,
              users.first_name,
              users.last_name,
              users.email,
              nfc_chips.action,
              CASE
                WHEN nfc_chips.action = 'EMPLOYEE_CHECK_IN' THEN 'industry_check_in'
                else 'non-industry_check_in'
              END as check_in_user_type,
              all_activation_descriptions,
              all_activation_event_ids,
              CASE
                WHEN all_activation_event_ids IS NOT NULL THEN 'activation'
                ELSE 'non_activation'
              END AS activation_checkin,
              restaurants.name as restaurant_name,
              concat(restaurants.name, '-', locations.name) as full_restaurant_location,
              restaurants.cohort as restaurant_cohort,
              restaurants.restaurant_id as checkin_restaurnt_id,
              locations.name as location_name,
              locations.location_id as checkin_location_id,
              locations.coordinate as checkin_location_coordinate,
              locations.city,
              restaurants.cuisine,
              neighborhoods.city as neighborhood_city,
              city_zip_codes_regions
            from
              checkins_ranked
              left join users on checkins_ranked.user_id = users.user_id
              left join locations on checkins_ranked.location_id = locations.location_id
              left join restaurants on locations.restaurant_id = restaurants.restaurant_id
              left join city_zip_codes_agg on locations.zipcode = city_zip_codes_agg.zip_code
              left join nfc_chips on checkins_ranked.nfc_chip_id = nfc_chips.nfc_chip_id
              left join neighborhoods on locations.neighborhood_id = neighborhoods.neighborhood_id
              left join activation_check_ins on checkins_ranked.check_in_id = activation_check_ins.check_in_id -- left join   user_tags on checkins_ranked.user_id = user_tags.user_id
            where
              checkins_ranked.restaurant_id not in (
                '2cb56d03-4417-4b60-afe3-be819ecde8ac',
                'e79c3d4e-ef0c-41de-829d-30ae5a75bf22',
                '7a717e76-34ed-4991-84f2-6797c1cb664b'
              )
            order by
              checkins_ranked.created_at at time zone 'america/new_york' at time zone 'utc' desc
          )
          select
            *
          from
            final
        ) c
    ),
    combined as (
      SELECT
        *
      FROM
        check_ins_stacked
      UNION ALL
      SELECT
        *
      FROM
        referrals_sent
      UNION ALL
      SELECT
        *
      FROM
        memberships_claimed
      UNION ALL
      SELECT
        *
      FROM
        collaborations_claimed
      UNION ALL
      SELECT
        *
      FROM
        messages_sent
    )
    select
      created_at_edt,
      user_id,
      activity_id,
      checkin_type as activity_type
    from
      combined_user_activities
    order by
      created_at_edt desc
  ) AS "source"
WHERE
  "source"."created_at_edt" >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))::timestamptz
  AND
  "source"."created_at_edt" < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz

GROUP BY
  CAST("source"."created_at_edt" AS date)
ORDER BY
  CAST("source"."created_at_edt" AS date) ASC
```

---

### Unique DAU Yesterday vs Trailing 4wk Avg

**Card ID:** 7836
**Description:** From [🐦‍⬛ CORE KPI] DAU, Today - Duplicate - Modified
**Tables Used:** `avg_prior_4weekdays_dau, check_ins, dau_by_date, prior_4weekdays, prior_4weekdays_dau, yesterday, yesterday_dau`

```sql
WITH dau_by_date AS (
  SELECT
    DATE(check_ins.created_at AT TIME ZONE 'America/New_York') AS date,
    COUNT(DISTINCT check_ins.user_id) AS dau
  FROM check_ins
  GROUP BY DATE(check_ins.created_at AT TIME ZONE 'America/New_York')
),
yesterday AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '1 day') AS dt
),
prior_4weekdays AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '8 day') AS date
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '15 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '22 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '29 day')
),
prior_4weekdays_dau AS (
  SELECT pw.date, dbd.dau
  FROM prior_4weekdays pw
  LEFT JOIN dau_by_date dbd ON dbd.date = pw.date
),
avg_prior_4weekdays_dau AS (
  SELECT AVG(dau::numeric) AS avg_dau
  FROM prior_4weekdays_dau
),
yesterday_dau AS (
  SELECT dau FROM dau_by_date, yesterday WHERE dau_by_date.date = yesterday.dt
)
SELECT
  y.dt AS calc_date,
  yd.dau AS yesterday_dau,
  apd.avg_dau AS trailing_4wk_avg,
  CASE
    WHEN apd.avg_dau IS NULL OR apd.avg_dau = 0 THEN NULL
    ELSE ROUND(CAST(100.0 * (yd.dau - apd.avg_dau) / apd.avg_dau AS numeric), 2)
  END AS pct_change_vs_4wk_avg
FROM yesterday y
LEFT JOIN yesterday_dau yd ON TRUE
LEFT JOIN avg_prior_4weekdays_dau apd ON TRUE;

```

---

### Check-Ins Yesterday vs Trailing 4wk Avg

**Card ID:** 7837
**Description:** From Yesterday Check In Count - Duplicate - Modified

Shows the count of check ins, grouped by how they were initiated. This DOES include employee check ins on the purple pucks.

NFC
URL - via joining a check
GPS
RESERVATION - via reservation notifcation
BEACON
**Tables Used:** `average_prior_weekdays, check_ins, counts, prior_weekdays, yesterday`

```sql
WITH prior_weekdays AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '8 day') AS date
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '15 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '22 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '29 day')
),
counts AS (
  SELECT
    pw.date,
    COUNT(c.check_in_id) AS cnt
  FROM prior_weekdays pw
  LEFT JOIN check_ins c ON DATE(c.created_at AT TIME ZONE 'America/New_York') = pw.date
  GROUP BY pw.date
),
average_prior_weekdays AS (
  SELECT AVG(cnt::numeric) AS avg_cnt FROM counts
),
yesterday AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '1 day') AS dt
),
yesterday_checkins AS (
  SELECT COUNT(distinct check_in_id) AS cnt
  FROM check_ins
  WHERE DATE(created_at AT TIME ZONE 'America/New_York') = (SELECT dt FROM yesterday)
)
SELECT
  y.dt AS calc_date,
  yc.cnt AS yesterday_checkins,
  apw.avg_cnt AS trailing_4wk_avg,
  CASE
    WHEN apw.avg_cnt IS NULL OR apw.avg_cnt = 0 THEN NULL
    ELSE ROUND(CAST(100.0 * (yc.cnt - apw.avg_cnt) / apw.avg_cnt AS numeric), 2)
  END AS pct_change_vs_4wk_avg
FROM average_prior_weekdays apw, yesterday y, yesterday_checkins yc;
```

---

### Daily Unique Paying Users 4wk

**Card ID:** 7856
**Tables Used:** `check_shares, checks, users`

```sql
SELECT
  DATE(check_shares.created_at AT TIME ZONE 'America/New_York') AS date,
  COUNT(DISTINCT check_shares.user_id) AS unique_users
FROM check_shares
JOIN checks ON checks.check_id = check_shares.check_id
JOIN users ON users.user_id = check_shares.user_id
WHERE
  checks.status = 'PAID'
  AND users.internal = false
  -- Only include dates from 29 days ago (relative to yesterday) up to yesterday
  AND DATE(check_shares.created_at AT TIME ZONE 'America/New_York')
      BETWEEN DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '29 days')
          AND DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '1 day')
GROUP BY DATE(check_shares.created_at AT TIME ZONE 'America/New_York')
ORDER BY date ASC;
```

---

### Unique Paying Users Yesterday vs Trailing 4wk Avg

**Card ID:** 7857
**Tables Used:** `base, check_shares, checks, prior_avg, prior_dates, prior_vals, users, yesterday_date, yesterday_val`

```sql
WITH base AS (
  SELECT
    DATE(check_shares.created_at AT TIME ZONE 'America/New_York') AS date,
    COUNT(DISTINCT check_shares.user_id) AS unique_users
  FROM check_shares
  JOIN checks ON checks.check_id = check_shares.check_id
  JOIN users ON users.user_id = check_shares.user_id
  WHERE
    checks.status = 'PAID'
    AND users.internal = false
    AND DATE(check_shares.created_at AT TIME ZONE 'America/New_York')
        BETWEEN DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '29 days')
            AND DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '1 day')
  GROUP BY DATE(check_shares.created_at AT TIME ZONE 'America/New_York')
),
yesterday_date AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '1 day') AS dt
),
yesterday_val AS (
  SELECT unique_users FROM base, yesterday_date WHERE base.date = yesterday_date.dt
),
prior_dates AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '8 day') AS dt
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '15 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '22 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '29 day')
),
prior_vals AS (
  SELECT unique_users
  FROM base
  JOIN prior_dates ON base.date = prior_dates.dt
),
prior_avg AS (
  SELECT AVG(unique_users::float) AS avg_unique_users FROM prior_vals
)
SELECT
  yd.dt AS calc_date,
  yv.unique_users AS unique_users_yesterday,
  pa.avg_unique_users AS trailing_4wk_avg,
  CASE
    WHEN pa.avg_unique_users IS NULL OR pa.avg_unique_users = 0 THEN NULL
    ELSE ROUND(CAST(100.0 * (yv.unique_users - pa.avg_unique_users) / pa.avg_unique_users AS numeric), 2)
  END AS pct_change_vs_4wk_avg
FROM yesterday_date yd
LEFT JOIN yesterday_val yv ON TRUE
LEFT JOIN prior_avg pa ON TRUE;

```

---

### Daily Check-ins / Live Location, 4wk

**Card ID:** 7858
**Description:** Consumer check-ins per # locations live on a given day. This does NOT include employee check ins on the purple pucks.
**Tables Used:** `check_in_counts, check_ins, location_summaries, locations, neighborhoods, nfc_chips`

```sql
WITH
  check_in_counts AS (
    SELECT
      DATE(ci.created_at AT TIME ZONE 'America/New_York') AS date,
      n.neighborhood_id,
      COUNT(DISTINCT (check_in_id)) AS check_in_count
    FROM
      check_ins ci
      JOIN locations l ON l.location_id = ci.location_id
      JOIN neighborhoods n ON n.neighborhood_id = l.neighborhood_id
      LEFT JOIN nfc_chips nfc ON nfc.nfc_chip_id = ci.nfc_chip_id
    WHERE
      ci.created_at >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))::timestamptz
      AND ci.created_at < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
      --AND nfc.action <> 'EMPLOYEE_CHECK_IN'
    GROUP BY 1,2
  )
SELECT
  ls.date,
  -- ls.neighborhood_id,
  SUM(ls.live) as total_live,
  SUM(ls.payments_enabled) as total_payments_enabled,
  COALESCE(SUM(cic.check_in_count), 0) as total_check_ins,
  CASE
        WHEN COALESCE(SUM(ls.live), 0) > 0
        THEN ROUND(COALESCE(SUM(cic.check_in_count), 0) * 1.0 / COALESCE(SUM(ls.live), 0), 2)
        ELSE 0
    END AS avg_check_ins_per_live_location
FROM
  location_summaries ls
  LEFT JOIN check_in_counts cic ON cic.neighborhood_id = ls.neighborhood_id
  AND ls.date = cic.date
WHERE
  ls.date >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))
GROUP BY ls.date

```

---

### Daily Downloads, 4wk

**Card ID:** 7860
**Tables Used:** `user_devices, user_first_download`

```sql
SELECT
  CAST("source"."time_first_downloaded_est" AS date) AS "date_first_downloaded_est",
  COUNT(*) AS "count"
FROM
  (
    WITH user_first_download AS (
      SELECT
        user_id,
        MIN(
          created_at AT TIME ZONE 'America/New_York'
        ) AS time_first_downloaded_est,
        'ios' as type
      FROM
        user_devices
      WHERE
        lower(user_agent) LIKE '%darwin%'
        AND lower(user_agent) NOT LIKE '%clip%'
      GROUP BY
        user_id
      UNION ALL
      SELECT
        user_id,
        MIN(
          created_at AT TIME ZONE 'America/New_York'
        ) AS time_first_downloaded_est,
        'android' as type
      FROM
        user_devices
      WHERE
        lower(user_agent) LIKE '%android%'
        AND lower(user_agent) NOT LIKE '%clip%'
      GROUP BY
        user_id
    )
    SELECT
      *
    FROM
      user_first_download
    ORDER BY
      time_first_downloaded_est DESC
  ) AS "source"
WHERE
  "source"."time_first_downloaded_est" >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))::timestamptz
  AND
  "source"."time_first_downloaded_est" < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
GROUP BY
  CAST("source"."time_first_downloaded_est" AS date)
ORDER BY
  CAST("source"."time_first_downloaded_est" AS date) ASC

```

---

### TPV Yesterday vs Trailing 4wk Avg

**Card ID:** 8053
**Tables Used:** `account_balances, account_transactions, all_transactions, all_transactions_daily, check_share_fly_redemptions, check_share_payments, check_shares, collab_card_renewals, collab_fly_redemptions, collab_purchases, collab_purchases_pre_fle, collaborations, coupon_card_swipes, coupon_fly_redemptions, fly_ledger_entries, misc_payment_links, payment_links, payments, pdr_deposit, pdr_final_charge, prior_4weekdays_tpv, prior_weekdays, private_dining_rooms, subscription_terms, users, yesterday_tpv`

```sql
WITH check_share_payments AS (
  SELECT
    'CHECK_SHARE' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    CAST(p.amount / 100.0 AS FLOAT) as adj_amount_usd,
    p.item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN check_shares cs ON fle.origin_id = cs.check_share_id
  WHERE p.status = 'SUCCEEDED'
    AND p.payment_method_id IS NOT NULL
    AND p.item_type IN ('CHECK_SHARE', 'FLY_AUTO_LOAD', 'CHECK')
    AND fle.origin_type = 'CHECK_SHARE'
    AND fle.credit_amount > 0
),

-- Direct collaboration purchases (not through FLE)
collab_purchases_pre_fle AS (
  SELECT
    'COLLAB - STRIPE/CHECKOUT' as transaction_type,
    p.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    p.user_id,
    p.amount / 100.0 as adj_amount_usd,
    p.item_id
  FROM payments p
  WHERE p.item_type = 'COLLAB'
    AND p.status = 'SUCCEEDED'
),

-- Check share FLY redemptions
check_share_fly_redemptions AS (
  SELECT
    'CHECK_SHARE_FLY_REDEMPTION' as transaction_type,
    cs.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    cs.user_id,
    fle.credit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM check_shares cs
  JOIN fly_ledger_entries fle ON fle.origin_id = cs.check_share_id
  WHERE fle.origin_type = 'CHECK_SHARE_REDEMPTION'
    AND fle.credit_amount > 0
),

-- Collaboration purchases through FLE
collab_purchases AS (
  SELECT
    'COLLAB' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^18 * 100.0) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM payments p
  JOIN fly_ledger_entries fle ON p.item_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id::text = u.user_id::text
  WHERE fle.origin_type = 'COLLAB'
    AND fle.debit_amount > 0
    AND ab.owner_type = 'USER'
    AND p.status = 'SUCCEEDED'
),

-- Collaboration FLY redemptions
collab_fly_redemptions AS (
  SELECT
    'COLLAB_FLY_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM account_transactions at
  JOIN collaborations c ON at.origin_id = c.collaboration_id
  JOIN fly_ledger_entries fle ON at.account_transaction_id = fle.account_transaction_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE at.origin_type = 'COLLAB_REDEMPTION'
    AND fle.debit_amount > 0
),

-- Collaboration renewals
collab_card_renewals AS (
  SELECT
    'COLLAB_RENEWAL' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    ab.owner_id as user_id,
    p.amount / 100.0 as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM subscription_terms st
  JOIN fly_ledger_entries fle ON fle.origin_id = st.subscription_term_id
  JOIN payments p ON fle.account_transaction_id = p.item_id
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  WHERE fle.debit_amount > 0
    AND fle.origin_type IN ('SUBCRIPTION_TERM', 'SUBSCRIPTION_TERM')
    AND p.status = 'SUCCEEDED'
),

-- Coupon card swipes
coupon_card_swipes AS (
  SELECT
    'COUPON_CARD_SWIPE' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  JOIN payments p ON p.item_id = fle.account_transaction_id
  WHERE fle.origin_type = 'COUPON'
    AND p.status = 'SUCCEEDED'
    AND fle.debit_amount > 0
),

-- Coupon FLY redemptions
coupon_fly_redemptions AS (
  SELECT
    'COUPON_REDEMPTION' as transaction_type,
    fle.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
    u.user_id,
    fle.debit_amount / (10^20) as adj_amount_usd,
    fle.account_transaction_id::uuid as item_id
  FROM fly_ledger_entries fle
  JOIN account_balances ab ON fle.account_balance_id = ab.account_balance_id
  JOIN users u ON ab.owner_id = u.user_id
  WHERE fle.origin_type = 'COUPON_REDEMPTION'
    AND fle.debit_amount > 0
),

pdr_final_charge AS (
   select 'PDR_FINAL_CHARGE' as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20) as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid as item_id
    from fly_ledger_entries
    join private_dining_rooms on private_dining_rooms.pdr_id = fly_ledger_entries.origin_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

pdr_deposit AS (
  select 'PDR_DEPOSIT'                                                 as transaction_type,
           fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
           account_balances.account_balance_id as user_id,
           fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
           fly_ledger_entries.account_transaction_id::uuid               as item_id
    from fly_ledger_entries
    join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
    join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
    join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
    where fly_ledger_entries.credit_amount > 0
),

misc_payment_links AS (
select 'MISC_PAYMENT_LINKS'                                                 as transaction_type,
               fly_ledger_entries.created_at AT TIME ZONE 'America/New_York' AT TIME ZONE 'UTC' AS created_at_edt,
               account_balances.account_balance_id,
               fly_ledger_entries.credit_amount / (10^20)                    as adj_amount_usd,
               fly_ledger_entries.account_transaction_id::uuid               as item_id
        from fly_ledger_entries
        join payment_links on payment_links.payment_link_id = fly_ledger_entries.origin_id
        left join private_dining_rooms on private_dining_rooms.payment_link_id = payment_links.payment_link_id
        join account_balances on account_balances.account_balance_id = fly_ledger_entries.account_balance_id
        where fly_ledger_entries.credit_amount > 0
        and private_dining_rooms.id is null -- NOT a private dining room
),

-- Combine all transaction types
all_transactions AS (
  SELECT * FROM check_share_payments
  UNION ALL
  SELECT * FROM check_share_fly_redemptions
  UNION ALL
  SELECT * FROM collab_purchases
  UNION ALL
  SELECT * FROM collab_purchases_pre_fle
  UNION ALL
  SELECT * FROM collab_fly_redemptions
  UNION ALL
  SELECT * FROM collab_card_renewals
  UNION ALL
  SELECT * FROM coupon_fly_redemptions
  UNION ALL
  SELECT * FROM coupon_card_swipes
  UNION ALL
  SELECT * FROM pdr_final_charge
  UNION ALL
  SELECT * FROM pdr_deposit
  UNION ALL
  SELECT * FROM misc_payment_links

),
all_transactions_daily AS (
SELECT
  DATE_TRUNC('day', created_at_edt) AS created_at_day,
  --transaction_type,
  --user_id,
  --item_id,
  SUM(adj_amount_usd) AS daily_tpv
FROM all_transactions
WHERE created_at_edt >= CAST(CAST((NOW() - INTERVAL '35 days') AS date) AS timestamptz)
    AND created_at_edt < CAST(CAST(NOW() AS date) AS timestamptz)
--WHERE created_at_edt >= (CAST((NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day') AS date))::timestamptz
--AND created_at_edt < (CAST((NOW() AT TIME ZONE 'America/New_York') AS date))::timestamptz
GROUP BY 1
),
yesterday AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '1 day') AS dt
),
prior_weekdays AS (
  SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '8 day') AS dt
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '15 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '22 day')
  UNION ALL SELECT DATE((NOW() AT TIME ZONE 'America/New_York') - INTERVAL '29 day')
),
yesterday_tpv AS (
  SELECT daily_tpv AS tpv
  FROM all_transactions_daily, yesterday
  WHERE all_transactions_daily.created_at_day = yesterday.dt
),
prior_4weekdays_tpv AS (
  SELECT
    atd.created_at_day,
    atd.daily_tpv
  FROM all_transactions_daily atd
  INNER JOIN prior_weekdays pw ON atd.created_at_day = pw.dt
),
prior_4weekdays_avg AS (
  SELECT AVG(daily_tpv) AS avg_tpv
  FROM prior_4weekdays_tpv
)
SELECT
  y.dt AS calc_date,
  yt.tpv AS yesterday_tpv,
  p4.avg_tpv AS trailing_4wk_avg,
  CASE
    WHEN p4.avg_tpv IS NULL OR p4.avg_tpv = 0 THEN NULL
    ELSE ROUND(CAST(100.0 * (yt.tpv - p4.avg_tpv) / p4.avg_tpv AS numeric), 2)
  END AS pct_change_vs_4wk_avg
FROM yesterday_tpv yt, prior_4weekdays_avg p4, yesterday y;

```

---

### Downloads Yesterday vs Trailing 4wk Avg

**Card ID:** 8086
**Description:** Downloads yesterday over an average of 4 weeks prior same day of week.
**Tables Used:** `downloads_by_date, prior_4weekdays, prior_avg, prior_vals, user_devices, user_first_download, yesterday, yesterday_val`

```sql
WITH user_first_download AS (
  SELECT
    user_id,
    MIN(created_at AT TIME ZONE 'America/New_York') AS time_first_downloaded_est,
    'ios' AS type
  FROM user_devices
  WHERE lower(user_agent) LIKE '%darwin%' AND lower(user_agent) NOT LIKE '%clip%'
  GROUP BY user_id

  UNION ALL

  SELECT
    user_id,
    MIN(created_at AT TIME ZONE 'America/New_York') AS time_first_downloaded_est,
    'android' AS type
  FROM user_devices
  WHERE lower(user_agent) LIKE '%android%' AND lower(user_agent) NOT LIKE '%clip%'
  GROUP BY user_id
),
downloads_by_date AS (
  SELECT
    CAST(time_first_downloaded_est AS date) AS date_first_downloaded_est,
    COUNT(*) AS cnt
  FROM user_first_download
  GROUP BY CAST(time_first_downloaded_est AS date)
),
yesterday AS (
  SELECT (NOW() AT TIME ZONE 'America/New_York' - INTERVAL '1 day')::date AS dt
),
prior_4weekdays AS (
  SELECT (NOW() AT TIME ZONE 'America/New_York' - INTERVAL '8 day')::date AS dt
  UNION ALL SELECT (NOW() AT TIME ZONE 'America/New_York' - INTERVAL '15 day')::date
  UNION ALL SELECT (NOW() AT TIME ZONE 'America/New_York' - INTERVAL '22 day')::date
  UNION ALL SELECT (NOW() AT TIME ZONE 'America/New_York' - INTERVAL '29 day')::date
),
yesterday_val AS (
  SELECT cnt
  FROM downloads_by_date, yesterday
  WHERE downloads_by_date.date_first_downloaded_est = yesterday.dt
),
prior_vals AS (
  SELECT cnt
  FROM downloads_by_date
  WHERE date_first_downloaded_est IN (SELECT dt FROM prior_4weekdays)
),
prior_avg AS (
  SELECT AVG(cnt::numeric) AS avg_val FROM prior_vals
)
SELECT
  y.dt AS calc_date,
  yv.cnt AS yesterday_first_downloads,
  pa.avg_val AS trailing_4wk_avg,
  CASE
    WHEN pa.avg_val IS NULL OR pa.avg_val = 0 THEN NULL
    ELSE ROUND(CAST(100.0 * (yv.cnt - pa.avg_val) / pa.avg_val AS numeric), 2)
  END AS pct_change_vs_4wk_avg
FROM yesterday y
LEFT JOIN yesterday_val yv ON TRUE
LEFT JOIN prior_avg pa ON TRUE;

```

---

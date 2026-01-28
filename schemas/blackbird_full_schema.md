# Blackbird Production Database Schema

**Database:** Coreprod Replica (Production)
**Engine:** PostgreSQL 14.12
**Database ID:** 69

## Schema: checkout

### Tables:

- sessions

### `checkout.sessions`

| Column                                                 | Type        | Semantic          | FK Target |
| ------------------------------------------------------ | ----------- | ----------------- | --------- |
| id                                                     | int4        | PK                |           |
| payload → acs → authentication_type                    | text        | Category          |           |
| payload → acs → challenge_cancel_reason                | text        | Category          |           |
| payload → acs → challenge_cancel_reason_code           | text        | Category          |           |
| payload → acs → challenge_mandated                     | boolean     |                   |           |
| payload → acs → operator_id                            | text        | Category          |           |
| payload → acs → reference_number                       | text        | Category          |           |
| payload → acs → transaction_id                         | text        | Category          |           |
| payload → acs → url                                    | text        | Category          |           |
| payload → amount                                       | decimal     |                   |           |
| payload → approved                                     | boolean     |                   |           |
| payload → authentication_category                      | text        | Category          |           |
| payload → authentication_date                          | text        | Category          |           |
| payload → authentication_type                          | text        | Category          |           |
| payload → body                                         | text        | SerializedJSON    |           |
| payload → cardholder_info                              | text        | Category          |           |
| payload → certificates → ds_public                     | text        | Category          |           |
| payload → challenged                                   | boolean     |                   |           |
| payload → challenge_indicator                          | text        | Category          |           |
| payload → cryptogram                                   | text        |                   |           |
| payload → currency                                     | text        | Category          |           |
| payload → ds → ds_id                                   | text        | Category          |           |
| payload → ds → reference_number                        | text        | Category          |           |
| payload → ds → transaction_id                          | text        | Category          |           |
| payload → eci                                          | text        | Category          |           |
| payload → exemption → applied                          | text        | Category          |           |
| payload → exemption → requested                        | text        | Category          |           |
| payload → exemption → trusted_beneficiary → source     | text        | Source            |           |
| payload → exemption → trusted_beneficiary → status     | text        | Category          |           |
| payload → flow_type                                    | text        | Category          |           |
| payload → http_status_code                             | decimal     |                   |           |
| payload → id                                           | text        |                   |           |
| payload → links → failure_url → href                   | text        | URL               |           |
| payload → links → self → href                          | text        | URL               |           |
| payload → links → success_url → href                   | text        | URL               |           |
| payload → next_actions                                 | text        |                   |           |
| payload → protocol_version                             | text        | Category          |           |
| payload → reference                                    | text        |                   |           |
| payload → request_id                                   | text        | Category          |           |
| payload → response_code                                | text        | Category          |           |
| payload → response_headers → Cko-Client-Id             | text        | Category          |           |
| payload → response_headers → Cko-Correlation-Id        | text        | Category          |           |
| payload → response_headers → Cko-Request-Id            | text        | Category          |           |
| payload → response_headers → Cko-Session-Source        | text        | Source            |           |
| payload → response_headers → Cko-Version               | text        | Category          |           |
| payload → response_headers → Connection                | text        | Category          |           |
| payload → response_headers → Content-Length            | text        | Category          |           |
| payload → response_headers → Content-Type              | text        | Category          |           |
| payload → response_headers → Date                      | text        | Category          |           |
| payload → response_headers → Strict-Transport-Security | text        | Category          |           |
| payload → response_status_reason                       | text        | Category          |           |
| payload → scheme                                       | text        | Category          |           |
| payload → self_link → href                             | text        | URL               |           |
| payload → session_secret                               | text        | Category          |           |
| payload → status                                       | text        | Category          |           |
| payload → status_reason                                | text        | Category          |           |
| payload → transaction_id                               | text        | Category          |           |
| payload → transaction_type                             | text        | Category          |           |
| payload → xid                                          | text        |                   |           |
| session_id                                             | uuid        |                   |           |
| external_session_id                                    | text        |                   |           |
| external_payment_id                                    | text        |                   |           |
| payload                                                | jsonb       | SerializedJSON    |           |
| created_at                                             | timestamptz | CreationTimestamp |           |
| updated_at                                             | timestamptz | UpdatedTimestamp  |           |

## Schema: gtm

### Tables:

- fly_contract_drops
- icp_restaurants

### `gtm.fly_contract_drops`

| Column              | Type    | Semantic | FK Target |
| ------------------- | ------- | -------- | --------- |
| id                  | int4    | PK       |           |
| restaurant_group_id | uuid    |          |           |
| allocation_fly      | numeric |          |           |

### `gtm.icp_restaurants`

| Column          | Type | Semantic | FK Target |
| --------------- | ---- | -------- | --------- |
| zipcode         | text | ZipCode  |           |
| icp_restaurants | int4 |          |           |

## Schema: hubspot

### Tables:

- deals
- owners

### `hubspot.deals`

| Column                                  | Type        | Semantic          | FK Target |
| --------------------------------------- | ----------- | ----------------- | --------- |
| id                                      | int4        | PK                |           |
| properties → bbx                        | text        | Category          |           |
| properties → bbx_category               | text        | Category          |           |
| properties → borough                    | text        | Category          |           |
| properties → churn_details              | text        |                   |           |
| properties → closed_lost                | text        |                   |           |
| properties → closed_lost_details        | text        |                   |           |
| properties → closed_lost_reason         | text        |                   |           |
| properties → date_of_trial_end          | text        |                   |           |
| properties → days_to_close              | text        |                   |           |
| properties → deal_interest_areas        | text        | Category          |           |
| properties → deal_scope                 | text        | Category          |           |
| properties → deal_source_details        | text        | Source            |           |
| properties → dealtype                   | text        | Category          |           |
| properties → demo_date                  | text        |                   |           |
| properties → description                | text        | Description       |           |
| properties → end_of_trial_date          | text        |                   |           |
| properties → fly_amount                 | text        | Category          |           |
| properties → fly_matched                | text        | Category          |           |
| properties → hubspot_owner_assigneddate | text        | Owner             |           |
| properties → hubspot_team_id            | text        | Category          |           |
| properties → initial_deal               | text        | Category          |           |
| properties → last_touch                 | text        | Category          |           |
| properties → new_deal_scope             | text        | Category          |           |
| properties → notes_last_contacted       | timestamp   |                   |           |
| properties → notes_last_updated         | timestamp   | UpdatedTimestamp  |           |
| properties → notes_next_activity_date   | text        | Category          |           |
| properties → onboarding_contact_email   | text        |                   |           |
| properties → onboarding_contact_nam     | text        |                   |           |
| properties → onboarding_stall_details   | text        |                   |           |
| properties → onboarding_stall_reasons   | text        | Category          |           |
| properties → pass_fee                   | text        | Category          |           |
| properties → pass_group                 | text        | Category          |           |
| properties → payments_live_date         | text        |                   |           |
| properties → postal_code                | text        | Category          |           |
| properties → processing_months_free     | text        | Category          |           |
| properties → rating                     | text        | Category          |           |
| properties → restaurant_name            | text        |                   |           |
| properties → sdr                        | text        | Category          |           |
| properties → transaction_fee            | text        | Category          |           |
| properties → win_reasons                | text        |                   |           |
| external_id                             | text        |                   |           |
| close_date                              | timestamptz |                   |           |
| create_date                             | timestamptz | CreationTimestamp |           |
| deal_name                               | text        |                   |           |
| deal_stage                              | text        | Category          |           |
| last_modified_date                      | timestamptz |                   |           |
| pipeline                                | text        | Category          |           |
| external_created_at                     | timestamptz | CreationTimestamp |           |
| external_updated_at                     | timestamptz | UpdatedTimestamp  |           |
| created_at                              | timestamptz | CreationTimestamp |           |
| updated_at                              | timestamptz | UpdatedTimestamp  |           |
| pass_sale_type                          | text        | Category          |           |
| owner_id                                | text        | Owner             |           |
| account_onboarding_owner_id             | text        | Owner             |           |
| reservation_platform                    | text        | Category          |           |
| pos_system                              | text        |                   |           |
| google_places_id                        | text        |                   |           |
| amount                                  | numeric     |                   |           |
| deal_source                             | text        | Source            |           |
| live_date                               | date        |                   |           |
| churn_date                              | date        |                   |           |
| churn_reason                            | text        |                   |           |
| tier                                    | text        |                   |           |
| market                                  | text        |                   |           |
| properties                              | jsonb       | SerializedJSON    |           |

### `hubspot.owners`

> HubSpot owner/user details for deal owner lookups

| Column              | Type        | Semantic          | FK Target |
| ------------------- | ----------- | ----------------- | --------- |
| id                  | int4        | PK                |           |
| external_id         | text        |                   |           |
| email               | varchar     | Email             |           |
| first_name          | varchar     | Name              |           |
| last_name           | varchar     |                   |           |
| user_id             | int8        |                   |           |
| archived            | bool        |                   |           |
| external_created_at | timestamptz | CreationTimestamp |           |
| external_updated_at | timestamptz | UpdatedTimestamp  |           |
| created_at          | timestamptz | CreationTimestamp |           |
| updated_at          | timestamptz | UpdatedTimestamp  |           |

## Schema: public

### Tables:

- account_balance_snapshots
- account_balances
- account_balances_aud
- account_transactions
- activation_events
- addresses
- adjustments
- banking_person_application_forms
- billing_addresses
- blackbird_payments
- blockchain_deposit_requests
- blockchain_fly_pay_requests
- blockchain_restaurant_location_contracts
- blockchain_transaction_requests
- blockchain_transactions
- budget_manager_action
- budget_manager_config
- cards
- check_ins
- check_shares
- check_shares_aud
- checks
- checks_aud
- chits
- city_zip_codes
- collaboration_perks
- collaboration_restaurants
- collaborations
- combined_user_activities
- conversation_messages
- conversations
- coupons
- cuisine_categories
- cuisines
- curated_recommendations
- employee_check_actions
- employee_incentive_progresses
- employee_incentives
- employee_pin_tokens
- employees
- evm_contracts
- experiments
- external_chit_payloads
- f2_distribution_configs
- f2_distributions
- failed_sessions
- fly_airdrop_batches
- fly_distribution_adjustments
- fly_ledger_entries
- fly_purchase_requests
- fly_throughput_snapshots
- flyway_schema_history
- geography_columns
- geometry_columns
- guest_book_entries
- image_urls
- incentive_reads
- incentives
- internal_chit_payloads
- internal_chit_payloads_mv
- ipfs_snapshots
- jobrunr_backgroundjobservers
- jobrunr_jobs
- jobrunr_jobs_stats
- jobrunr_metadata
- jobrunr_migrations
- jobrunr_recurring_jobs
- launch_info
- location_ai_data
- location_summaries
- location_weekly_reports
- locations
- locations_aud
- locations_updates
- media
- media_promotions
- membership_events
- membership_tiers
- memberships
- menu_option_sets
- neighborhood_zipcodes
- neighborhoods
- nfc_chips
- nft_airdrop_batches
- nft_mint_batches
- nft_supply_counts
- nfts
- open_hours
- opentable_guests
- passes
- passes_aud
- pay_settings
- payment_links
- payments
- payout_accounts
- payouts
- pg_stat_statements
- pg_stat_statements_info
- popular_restaurants_view
- ppx_entries
- press_checks_backup
- private_dining_rooms
- promo_codes
- promotion_applications
- promotion_codes
- promotion_redemptions
- ranked_fly_throughput_view
- referral_codes
- referrals
- refunds
- regions
- reservation_requests
- reservations
- restaurant_attributes
- restaurant_events
- restaurant_groups
- restaurant_list_entries
- restaurant_lists
- restaurant_master_keys
- restaurant_recommendations
- restaurant_user_integrations
- restaurant_users
- restaurant_users_locations
- restaurants
- restaurants_cuisines
- revinfo
- reward_listings
- reward_rules
- rewards
- scheduled_gift_emails
- scheduled_worker_runs
- service_configurations
- statuses
- subscription_terms
- sun_data_entries
- temp_darsh_loctions
- user_cuisine_category_scores
- user_devices
- user_incentive_activities
- user_incentives
- user_media_views
- user_notifications
- user_preferences
- user_price_scores
- user_status_overrides
- user_status_progress
- user_statuses
- user_statuses_aud
- user_tags
- user_terms
- user_wallet_permits
- user_wallets
- users
- users_aud
- users_neighborhoods_scores
- waitlist_entries
- wallet_signatures
- webhook_events

### `public.account_balance_snapshots`

| Column             | Type        | Semantic         | FK Target |
| ------------------ | ----------- | ---------------- | --------- |
| id                 | int4        | PK               |           |
| snapshot_id        | uuid        | Category         |           |
| snapshot_timestamp | timestamptz |                  |           |
| account_owner_type | text        | Category         |           |
| account_owner_id   | uuid        | Owner            |           |
| balance            | numeric     |                  |           |
| account_updated_at | timestamptz | UpdatedTimestamp |           |
| airdrop_batch_id   | uuid        |                  |           |
| user_wallet_id     | uuid        |                  |           |

### `public.account_balances`

| Column                    | Type        | Semantic          | FK Target |
| ------------------------- | ----------- | ----------------- | --------- |
| id                        | int4        | PK                |           |
| account_balance_id        | uuid        |                   |           |
| owner_type                | text        | Category          |           |
| owner_id                  | uuid        | Owner             |           |
| currency                  | text        | Category          |           |
| balance                   | numeric     |                   |           |
| created_at                | timestamptz | CreationTimestamp |           |
| updated_at                | timestamptz | UpdatedTimestamp  |           |
| treasury_prime_account_id | text        | FK                |           |
| version                   | int4        | Category          |           |

### `public.account_balances_aud`

| Column     | Type        | Semantic          | FK Target          |
| ---------- | ----------- | ----------------- | ------------------ |
| id         | int4        | PK                |                    |
| rev        | int4        | FK                | public.revinfo.rev |
| revtype    | int2        | Category          |                    |
| balance    | numeric     |                   |                    |
| created_at | timestamptz | CreationTimestamp |                    |

### `public.account_transactions`

| Column                 | Type        | Semantic          | FK Target                                      |
| ---------------------- | ----------- | ----------------- | ---------------------------------------------- |
| id                     | int4        | PK                |                                                |
| account_transaction_id | uuid        |                   |                                                |
| origin_type            | text        | Category          |                                                |
| origin_id              | uuid        |                   |                                                |
| created_at             | timestamptz | CreationTimestamp |                                                |
| updated_at             | timestamptz | UpdatedTimestamp  |                                                |
| blackbird_payment_id   | uuid        | FK                | public.blackbird_payments.blackbird_payment_id |

### `public.activation_events`

| Column              | Type        | Semantic          | FK Target                    |
| ------------------- | ----------- | ----------------- | ---------------------------- |
| id                  | int4        | PK                |                              |
| activation_event_id | uuid        | PK                |                              |
| location_id         | uuid        | FK                | public.locations.location_id |
| description         | text        | Description       |                              |
| start_date          | timestamp   | CreationTimestamp |                              |
| end_date            | timestamp   |                   |                              |
| created_at          | timestamptz | CreationTimestamp |                              |
| updated_at          | timestamptz | UpdatedTimestamp  |                              |

### `public.addresses`

| Column     | Type    | Semantic | FK Target |
| ---------- | ------- | -------- | --------- |
| id         | uuid    | PK       |           |
| nonce      | numeric |          |           |
| address    | text    | Category |           |
| chain_type | text    | Category |           |

### `public.adjustments`

| Column               | Type        | Semantic | FK Target                          |
| -------------------- | ----------- | -------- | ---------------------------------- |
| id                   | int4        | PK       |                                    |
| adjustment_id        | uuid        |          |                                    |
| amount               | int8        |          |                                    |
| fly_amount           | int8        |          |                                    |
| house_account_amount | int8        |          |                                    |
| usd_amount           | int8        |          |                                    |
| currency             | text        |          |                                    |
| check_share_id       | uuid        | FK       | public.check_shares.check_share_id |
| reason               | text        |          |                                    |
| comment              | text        |          |                                    |
| status               | text        |          |                                    |
| external_id          | text        |          |                                    |
| provider             | text        |          |                                    |
| payout_id            | uuid        | FK       | public.payouts.payout_id           |
| created_at           | timestamptz |          |                                    |
| updated_at           | timestamptz |          |                                    |

### `public.banking_person_application_forms`

| Column                               | Type        | Semantic | FK Target                                  |
| ------------------------------------ | ----------- | -------- | ------------------------------------------ |
| id                                   | int4        | PK       |                                            |
| banking_person_application_form_id   | uuid        |          |                                            |
| restaurant_user_id                   | uuid        | FK       | public.restaurant_users.restaurant_user_id |
| first_name                           | text        |          |                                            |
| last_name                            | text        |          |                                            |
| email_address                        | text        |          |                                            |
| treasury_prime_person_application_id | text        | FK       |                                            |
| created_at                           | timestamptz |          |                                            |
| updated_at                           | timestamptz |          |                                            |

### `public.billing_addresses`

| Column             | Type        | Semantic          | FK Target            |
| ------------------ | ----------- | ----------------- | -------------------- |
| id                 | int4        | PK                |                      |
| billing_address_id | uuid        |                   |                      |
| user_id            | uuid        | FK                | public.users.user_id |
| street             | text        |                   |                      |
| street2            | text        |                   |                      |
| city               | text        | City              |                      |
| state              | text        | State             |                      |
| zipcode            | text        | ZipCode           |                      |
| created_at         | timestamptz | CreationTimestamp |                      |
| updated_at         | timestamptz | UpdatedTimestamp  |                      |
| country            | text        | Country           |                      |

### `public.blackbird_payments`

| Column               | Type        | Semantic          | FK Target                                |
| -------------------- | ----------- | ----------------- | ---------------------------------------- |
| id                   | int4        | PK                |                                          |
| blackbird_payment_id | uuid        |                   |                                          |
| user_id              | uuid        | FK                | public.users.user_id                     |
| item_id              | uuid        |                   |                                          |
| item_type            | text        | Category          |                                          |
| card_id              | uuid        |                   |                                          |
| card_type            | text        | Category          |                                          |
| card_payment_id      | uuid        | FK                | public.payments.payment_id               |
| promotion_code_id    | uuid        | FK                | public.promotion_codes.promotion_code_id |
| discount_total       | int8        | Discount          |                                          |
| card_total           | int8        |                   |                                          |
| wallet_total         | int8        | Category          |                                          |
| house_account_total  | int8        | Category          |                                          |
| fly_total            | int8        | Category          |                                          |
| total                | int8        |                   |                                          |
| status               | text        | Category          |                                          |
| created_at           | timestamptz | CreationTimestamp |                                          |
| updated_at           | timestamptz | UpdatedTimestamp  |                                          |

### `public.blockchain_deposit_requests`

| Column             | Type        | Semantic          | FK Target |
| ------------------ | ----------- | ----------------- | --------- |
| id                 | int4        | PK                |           |
| signature_id       | uuid        | Category          |           |
| created_at         | timestamptz | CreationTimestamp |           |
| updated_at         | timestamptz | UpdatedTimestamp  |           |
| status             | text        | Category          |           |
| block_hash         | text        | Category          |           |
| wallet_id          | uuid        | Category          |           |
| transaction_id     | uuid        | Category          |           |
| value_amount       | numeric     |                   |           |
| deposit_request_id | uuid        |                   |           |

### `public.blockchain_fly_pay_requests`

| Column             | Type        | Semantic          | FK Target |
| ------------------ | ----------- | ----------------- | --------- |
| id                 | uuid        | PK                |           |
| signature_id       | uuid        | Category          |           |
| origin_id          | uuid        | Category          |           |
| origin_type        | text        | Category          |           |
| created_at         | timestamptz | CreationTimestamp |           |
| updated_at         | timestamptz | UpdatedTimestamp  |           |
| status             | text        | Category          |           |
| wallet_id          | uuid        | Category          |           |
| spent_amount       | numeric     |                   |           |
| transaction_id     | uuid        |                   |           |
| mint_amount        | numeric     |                   |           |
| purchase_origin_id | uuid        |                   |           |
| to_address         | text        | Category          |           |

### `public.blockchain_restaurant_location_contracts`

| Column                   | Type        | Semantic          | FK Target |
| ------------------------ | ----------- | ----------------- | --------- |
| id                       | uuid        | PK                |           |
| location_id              | uuid        |                   |           |
| contract_id              | uuid        |                   |           |
| transaction_id           | uuid        |                   |           |
| address                  | text        | Category          |           |
| owner_address            | text        | Owner             |           |
| restaurant_owner_address | text        | Owner             |           |
| created_at               | timestamptz | CreationTimestamp |           |
| updated_at               | timestamptz | UpdatedTimestamp  |           |

### `public.blockchain_transaction_requests`

| Column                   | Type        | Semantic          | FK Target |
| ------------------------ | ----------- | ----------------- | --------- |
| id                       | uuid        | PK                |           |
| created_at               | timestamptz | CreationTimestamp |           |
| max_fee_per_gas          | numeric     |                   |           |
| raw_data                 | text        |                   |           |
| signed_data              | text        |                   |           |
| transaction_id           | uuid        |                   |           |
| base_fee                 | numeric     |                   |           |
| max_priority_fee_per_gas | numeric     |                   |           |

### `public.blockchain_transactions`

| Column           | Type        | Semantic          | FK Target |
| ---------------- | ----------- | ----------------- | --------- |
| id               | uuid        | PK                |           |
| created_at       | timestamptz | CreationTimestamp |           |
| request_id       | uuid        |                   |           |
| address_id       | uuid        | Category          |           |
| to_address       | text        | Category          |           |
| status           | text        | Category          |           |
| nonce            | numeric     |                   |           |
| gas_limit        | numeric     |                   |           |
| gas_used         | numeric     |                   |           |
| transaction_hash | text        |                   |           |
| encoded_function | text        |                   |           |
| budget_action_id | uuid        | Category          |           |
| chain_type       | text        | Category          |           |
| version          | int4        | Category          |           |
| tx_type          | text        | Category          |           |
| native_value     | numeric     |                   |           |

### `public.budget_manager_action`

| Column           | Type    | Semantic | FK Target |
| ---------------- | ------- | -------- | --------- |
| id               | int4    | PK       |           |
| budget_action_id | uuid    | Category |           |
| worker_name      | text    | Category |           |
| worker_table     | text    | Category |           |
| runs_per_day     | numeric |          |           |

### `public.budget_manager_config`

| Column                    | Type        | Semantic         | FK Target |
| ------------------------- | ----------- | ---------------- | --------- |
| id                        | int4        | PK               |           |
| last_budget_update        | timestamptz | UpdatedTimestamp |           |
| profile_name              | text        | Category         |           |
| daily_spend_target        | numeric     |                  |           |
| maximum_overspend_percent | numeric     | Share            |           |
| current_budget            | numeric     |                  |           |

### `public.cards`

| Column                            | Type        | Semantic          | FK Target                                   |
| --------------------------------- | ----------- | ----------------- | ------------------------------------------- |
| id                                | int4        | PK                |                                             |
| card_id                           | uuid        |                   |                                             |
| user_id                           | uuid        | FK                | public.users.user_id                        |
| provider                          | text        | Category          |                                             |
| token                             | text        |                   |                                             |
| status                            | text        | Category          |                                             |
| expiration_month                  | int4        | Category          |                                             |
| expiration_year                   | int4        | Category          |                                             |
| brand                             | text        | Category          |                                             |
| last4                             | text        |                   |                                             |
| bin                               | text        |                   |                                             |
| card_type                         | text        | Category          |                                             |
| card_category                     | text        | Category          |                                             |
| issuer_country                    | text        | Country           |                                             |
| product_id                        | text        | Category          |                                             |
| product_type                      | text        | Category          |                                             |
| is_default                        | bool        |                   |                                             |
| cardholder_name                   | text        | Category          |                                             |
| expires_at                        | timestamptz |                   |                                             |
| created_at                        | timestamptz | CreationTimestamp |                                             |
| updated_at                        | timestamptz | UpdatedTimestamp  |                                             |
| billing_address_id                | uuid        | FK                | public.billing_addresses.billing_address_id |
| fingerprint                       | text        |                   |                                             |
| wallet_type                       | text        | Category          |                                             |
| zipcode                           | text        | ZipCode           |                                             |
| authorization_external_payment_id | text        | Author            |                                             |
| display_name                      | text        |                   |                                             |

### `public.check_ins`

| Column                 | Type        | Semantic          | FK Target                        |
| ---------------------- | ----------- | ----------------- | -------------------------------- |
| id                     | int4        | PK                |                                  |
| check_in_id            | uuid        |                   |                                  |
| nfc_chip_id            | uuid        | FK                | public.nfc_chips.nfc_chip_id     |
| user_id                | uuid        | FK                | public.users.user_id             |
| created_at             | timestamptz | CreationTimestamp |                                  |
| updated_at             | timestamptz | UpdatedTimestamp  |                                  |
| restaurant_id          | uuid        | FK                | public.restaurants.restaurant_id |
| membership_id          | uuid        | FK                | public.memberships.membership_id |
| location_id            | uuid        |                   |                                  |
| restaurant_visit_count | int4        | Quantity          |                                  |
| entry_id               | uuid        |                   |                                  |
| ended_at               | timestamptz |                   |                                  |
| payment_funnel_type    | text        | Category          |                                  |
| initiation_type        | text        | Category          |                                  |
| hidden_at              | timestamptz |                   |                                  |
| \_created_at_edt       | timestamp   | CreationTimestamp |                                  |
| intent_step_seen       | bool        |                   |                                  |

### `public.check_shares`

| Column                                  | Type        | Semantic          | FK Target                    |
| --------------------------------------- | ----------- | ----------------- | ---------------------------- |
| id                                      | int4        | PK                |                              |
| check_share_id                          | uuid        |                   |                              |
| check_id                                | uuid        | FK                | public.checks.check_id       |
| user_id                                 | uuid        | FK                | public.users.user_id         |
| payment_method_id                       | uuid        | FK                | public.cards.card_id         |
| house_account_fly_credit                | numeric     |                   |                              |
| check_share_total                       | int8        |                   |                              |
| gratuity_preference_value               | int8        | Category          |                              |
| gratuity_preference_type                | text        | Category          |                              |
| created_at                              | timestamptz | CreationTimestamp |                              |
| updated_at                              | timestamptz | UpdatedTimestamp  |                              |
| is_party_host                           | bool        |                   |                              |
| check_in_id                             | uuid        | FK                | public.check_ins.check_in_id |
| gratuity                                | int8        | Category          |                              |
| apply_fly_balance                       | bool        |                   |                              |
| fly_credit                              | numeric     |                   |                              |
| user_identifying_order_item_provider_id | uuid        |                   |                              |
| service_charges                         | int8        | Category          |                              |

### `public.check_shares_aud`

| Column            | Type        | Semantic          | FK Target          |
| ----------------- | ----------- | ----------------- | ------------------ |
| id                | int4        | PK                |                    |
| rev               | int4        | FK                | public.revinfo.rev |
| revtype           | int2        | Category          |                    |
| payment_method_id | uuid        |                   |                    |
| created_at        | timestamptz | CreationTimestamp |                    |

### `public.checks`

| Column                  | Type        | Semantic          | FK Target                    |
| ----------------------- | ----------- | ----------------- | ---------------------------- |
| id                      | int4        | PK                |                              |
| check_id                | uuid        |                   |                              |
| pos_provider_id         | uuid        | Category          |                              |
| pos_provider            | text        | Category          |                              |
| status                  | text        | Category          |                              |
| created_at              | timestamptz | CreationTimestamp |                              |
| updated_at              | timestamptz | UpdatedTimestamp  |                              |
| party_size              | int8        | Category          |                              |
| total                   | int8        |                   |                              |
| sub_total               | int8        |                   |                              |
| tax                     | int8        |                   |                              |
| discounts               | int8        | Discount          |                              |
| due                     | int8        |                   |                              |
| gratuity                | int8        |                   |                              |
| service_charges         | int8        | Category          |                              |
| other_charges           | int8        | Category          |                              |
| amount_paid             | int8        |                   |                              |
| num_items               | int4        | Quantity          |                              |
| pos_provider_check_id   | uuid        |                   |                              |
| location_id             | uuid        | FK                | public.locations.location_id |
| payment_method_id       | uuid        | FK                | public.cards.card_id         |
| payout_id               | uuid        | FK                | public.payouts.payout_id     |
| webhook_updated_at      | timestamptz | UpdatedTimestamp  |                              |
| bb_payment_total        | int8        | Category          |                              |
| service_type            | text        | Category          |                              |
| gratuity_value          | int8        |                   |                              |
| gratuity_type           | text        | Category          |                              |
| expires_at              | timestamptz |                   |                              |
| bb_credit_total         | int8        | Category          |                              |
| payment_scenario        | text        | Category          |                              |
| pos_provider_request_id | uuid        |                   |                              |
| has_late_webhook        | bool        |                   |                              |
| table_number            | text        |                   |                              |
| in_store_code           | varchar     |                   |                              |
| check_number            | text        |                   |                              |
| prepayment              | int8        |                   |                              |
| bb_fee_cents            | int8        | Category          |                              |
| closing_employee_id     | uuid        | FK                | public.employees.employee_id |
| paid_at                 | timestamptz |                   |                              |

### `public.checks_aud`

| Column            | Type        | Semantic          | FK Target          |
| ----------------- | ----------- | ----------------- | ------------------ |
| id                | int4        | PK                |                    |
| rev               | int4        | FK                | public.revinfo.rev |
| revtype           | int2        | Category          |                    |
| payment_method_id | uuid        |                   |                    |
| created_at        | timestamptz | CreationTimestamp |                    |

### `public.chits`

| Column                       | Type        | Semantic          | FK Target            |
| ---------------------------- | ----------- | ----------------- | -------------------- |
| id                           | int4        | PK                |                      |
| chit_id                      | uuid        |                   |                      |
| user_id                      | uuid        | FK                | public.users.user_id |
| internal_blurb               | text        |                   |                      |
| created_at                   | timestamptz | CreationTimestamp |                      |
| updated_at                   | timestamptz | UpdatedTimestamp  |                      |
| external_blurb               | text        | Category          |                      |
| blurb                        | text        | Category          |                      |
| internal_blurb_system_prompt | text        | Category          |                      |
| external_blurb_system_prompt | text        | Category          |                      |
| summary_blurb_system_prompt  | text        | Category          |                      |
| hint                         | text        | Category          |                      |

### `public.city_zip_codes`

| Column           | Type | Semantic | FK Target |
| ---------------- | ---- | -------- | --------- |
| id               | int4 | PK       |           |
| city_zip_code_id | uuid |          |           |
| zip_code         | text | ZipCode  |           |
| city             | text | City     |           |
| region           | text |          |           |

### `public.collaboration_perks`

| Column           | Type      | Semantic          | FK Target                              |
| ---------------- | --------- | ----------------- | -------------------------------------- |
| collab_perk_id   | uuid      | PK                |                                        |
| collaboration_id | uuid      | FK                | public.collaborations.collaboration_id |
| title            | text      | Title             |                                        |
| description      | text      | Description       |                                        |
| id               | int4      | PK                |                                        |
| created_at       | timestamp | CreationTimestamp |                                        |
| updated_at       | timestamp | UpdatedTimestamp  |                                        |

### `public.collaboration_restaurants`

| Column           | Type        | Semantic          | FK Target                              |
| ---------------- | ----------- | ----------------- | -------------------------------------- |
| id               | int4        | PK                |                                        |
| collaboration_id | uuid        | FK                | public.collaborations.collaboration_id |
| restaurant_id    | uuid        | FK                | public.restaurants.restaurant_id       |
| created_at       | timestamptz | CreationTimestamp |                                        |
| updated_at       | timestamptz | UpdatedTimestamp  |                                        |

### `public.collaborations`

| Column                        | Type        | Semantic          | FK Target                |
| ----------------------------- | ----------- | ----------------- | ------------------------ |
| id                            | int4        | PK                |                          |
| collaboration_id              | uuid        | Category          |                          |
| name                          | text        | Name              |                          |
| description                   | text        | Description       |                          |
| expiration_date               | date        |                   |                          |
| image                         | text        | URL               |                          |
| benefits                      | text        | SerializedJSON    |                          |
| created_at                    | timestamptz | CreationTimestamp |                          |
| updated_at                    | timestamptz | UpdatedTimestamp  |                          |
| artist                        | text        | Category          |                          |
| url                           | text        | URL               |                          |
| price_usd                     | int8        | Category          |                          |
| email_template_id             | text        | Category          |                          |
| payment_image                 | text        | URL               |                          |
| sale_start_date               | date        | CreationDate      |                          |
| sale_end_date                 | date        |                   |                          |
| primary_region_id             | uuid        | FK                | public.regions.region_id |
| promo_description             | text        | Description       |                          |
| expiration_type               | text        | Category          |                          |
| expiration_period             | text        | Category          |                          |
| state                         | text        | Category          |                          |
| active_start_time             | time        | CreationTime      |                          |
| active_end_time               | time        |                   |                          |
| waitlist_email_template_id    | text        |                   |                          |
| primary_reward                | text        | Category          |                          |
| terms                         | text        | SerializedJSON    |                          |
| renewable                     | bool        |                   |                          |
| terms_full                    | text        | SerializedJSON    |                          |
| slug                          | text        | Category          |                          |
| quantity_sold                 | int4        | Quantity          |                          |
| max_quantity                  | int4        | Quantity          |                          |
| unsubscribe_email_template_id | text        |                   |                          |
| background_color              | varchar     | Category          |                          |
| about                         | text        | Category          |                          |
| text_color                    | varchar     | Category          |                          |
| confirmation_email_image      | text        |                   |                          |
| confirmation_email_copy       | text        |                   |                          |
| waitlist_email_copy           | text        |                   |                          |
| level_2_sale_start_date       | date        | CreationDate      |                          |
| level_3_sale_start_date       | date        | CreationDate      |                          |
| level_4_sale_start_date       | date        | CreationDate      |                          |

### `public.combined_user_activities`

| Column         | Type        | Semantic          | FK Target |
| -------------- | ----------- | ----------------- | --------- |
| created_at_edt | timestamptz | CreationTimestamp |           |
| user_id        | text        |                   |           |
| activity_id    | text        |                   |           |
| checkin_type   | text        | Category          |           |

### `public.conversation_messages`

| Column                | Type        | Semantic          | FK Target               |
| --------------------- | ----------- | ----------------- | ----------------------- |
| id                    | int4        | PK                |                         |
| provider_id           | text        | Category          |                         |
| conversation_id       | int4        | FK                | public.conversations.id |
| author                | text        | Author            |                         |
| author_type           | text        | Category          |                         |
| author_participant_id | text        | Author            |                         |
| body                  | text        | Category          |                         |
| index                 | int4        | Category          |                         |
| timestamp             | timestamptz |                   |                         |
| created_at            | timestamptz | CreationTimestamp |                         |
| updated_at            | timestamptz | UpdatedTimestamp  |                         |

### `public.conversations`

| Column                   | Type        | Semantic          | FK Target                    |
| ------------------------ | ----------- | ----------------- | ---------------------------- |
| id                       | int4        | PK                |                              |
| conversation_provider_id | text        |                   |                              |
| location_id              | uuid        | FK                | public.locations.location_id |
| user_id                  | uuid        | FK                | public.users.user_id         |
| unique_name              | text        |                   |                              |
| conversation_type        | text        | Category          |                              |
| created_at               | timestamptz | CreationTimestamp |                              |
| updated_at               | timestamptz | UpdatedTimestamp  |                              |
| active                   | bool        |                   |                              |

### `public.coupons`

| Column             | Type        | Semantic          | FK Target |
| ------------------ | ----------- | ----------------- | --------- |
| id                 | int4        | PK                |           |
| coupon_id          | uuid        | Category          |           |
| amount_off         | int8        |                   |           |
| duration           | text        | Category          |           |
| duration_in_months | int4        | Duration          |           |
| active             | bool        |                   |           |
| max_redemptions    | int4        | Category          |           |
| name               | varchar     | Name              |           |
| percent_off        | float8      | Share             |           |
| redeem_by          | timestamptz |                   |           |
| times_redeemed     | int4        | Category          |           |
| created_at         | timestamptz | CreationTimestamp |           |
| updated_at         | timestamptz | UpdatedTimestamp  |           |
| item_id            | uuid        | Category          |           |
| item_type          | text        | Category          |           |
| purchasable        | bool        |                   |           |

### `public.cuisine_categories`

| Column              | Type        | Semantic          | FK Target |
| ------------------- | ----------- | ----------------- | --------- |
| id                  | int4        | PK                |           |
| cuisine_category_id | uuid        | PK                |           |
| name                | text        | Name              |           |
| created_at          | timestamptz | CreationTimestamp |           |
| updated_at          | timestamptz | UpdatedTimestamp  |           |

### `public.cuisines`

| Column              | Type        | Semantic          | FK Target                                     |
| ------------------- | ----------- | ----------------- | --------------------------------------------- |
| id                  | int4        | PK                |                                               |
| cuisine_id          | uuid        | PK                |                                               |
| cuisine_category_id | uuid        | FK                | public.cuisine_categories.cuisine_category_id |
| name                | text        | Name              |                                               |
| created_at          | timestamptz | CreationTimestamp |                                               |
| updated_at          | timestamptz | UpdatedTimestamp  |                                               |

### `public.curated_recommendations`

| Column                    | Type        | Semantic          | FK Target                    |
| ------------------------- | ----------- | ----------------- | ---------------------------- |
| id                        | int4        | PK                |                              |
| curated_recommendation_id | uuid        |                   |                              |
| region_id                 | uuid        | FK                | public.regions.region_id     |
| location_id               | uuid        | FK                | public.locations.location_id |
| category                  | text        | Category          |                              |
| month                     | int4        |                   |                              |
| year                      | int4        |                   |                              |
| created_at                | timestamptz | CreationTimestamp |                              |
| updated_at                | timestamptz | UpdatedTimestamp  |                              |

### `public.employee_check_actions`

| Column      | Type        | Semantic          | FK Target                    |
| ----------- | ----------- | ----------------- | ---------------------------- |
| id          | int4        | PK                |                              |
| employee_id | uuid        | FK                | public.employees.employee_id |
| check_id    | uuid        | FK                | public.checks.check_id       |
| action      | text        | Category          |                              |
| created_at  | timestamptz | CreationTimestamp |                              |
| updated_at  | timestamptz | UpdatedTimestamp  |                              |

### `public.employee_incentive_progresses`

| Column                         | Type        | Semantic | FK Target                                        |
| ------------------------------ | ----------- | -------- | ------------------------------------------------ |
| id                             | int4        | PK       |                                                  |
| employee_incentive_progress_id | uuid        |          |                                                  |
| employee_id                    | uuid        | FK       | public.employees.employee_id                     |
| employee_incentive_id          | uuid        | FK       | public.employee_incentives.employee_incentive_id |
| progress                       | int4        |          |                                                  |
| created_at                     | timestamptz |          |                                                  |
| updated_at                     | timestamptz |          |                                                  |

### `public.employee_incentives`

| Column                  | Type      | Semantic | FK Target                    |
| ----------------------- | --------- | -------- | ---------------------------- |
| id                      | int4      | PK       |                              |
| employee_incentive_id   | uuid      |          |                              |
| location_id             | uuid      | FK       | public.locations.location_id |
| starts_at               | timestamp |          |                              |
| ends_at                 | timestamp |          |                              |
| created_at              | timestamp |          |                              |
| updated_at              | timestamp |          |                              |
| status                  | text      |          |                              |
| target                  | int4      |          |                              |
| group_reward_cents      | int4      |          |                              |
| individual_reward_cents | int4      |          |                              |
| completed_at            | timestamp |          |                              |

### `public.employee_pin_tokens`

| Column      | Type        | Semantic          | FK Target                    |
| ----------- | ----------- | ----------------- | ---------------------------- |
| id          | int8        | PK                |                              |
| token       | text        | Category          |                              |
| employee_id | uuid        | FK                | public.employees.employee_id |
| expires_at  | timestamptz |                   |                              |
| created_at  | timestamptz | CreationTimestamp |                              |
| updated_at  | timestamptz | UpdatedTimestamp  |                              |

### `public.employees`

| Column         | Type        | Semantic          | FK Target                    |
| -------------- | ----------- | ----------------- | ---------------------------- |
| id             | int4        | PK                |                              |
| user_id        | uuid        | FK                | public.users.user_id         |
| location_id    | uuid        | FK                | public.locations.location_id |
| active         | bool        |                   |                              |
| created_at     | timestamptz | CreationTimestamp |                              |
| updated_at     | timestamptz | UpdatedTimestamp  |                              |
| employee_id    | uuid        |                   |                              |
| last_active_at | timestamptz |                   |                              |
| pin            | varchar     |                   |                              |

### `public.evm_contracts`

| Column                 | Type        | Semantic       | FK Target |
| ---------------------- | ----------- | -------------- | --------- |
| id                     | uuid        | PK             |           |
| contract_type          | text        |                |           |
| contract_address       | text        |                |           |
| deployer_address       | text        |                |           |
| implementation_address | text        |                |           |
| abi                    | jsonb       | SerializedJSON |           |
| bytecode               | text        |                |           |
| is_proxy               | bool        |                |           |
| deployed_at            | timestamptz |                |           |
| created_at             | timestamptz |                |           |

### `public.experiments`

| Column     | Type        | Semantic          | FK Target |
| ---------- | ----------- | ----------------- | --------- |
| user_id    | uuid        |                   |           |
| experiment | text        | Category          |           |
| treatment  | text        | Category          |           |
| created_at | timestamptz | CreationTimestamp |           |
| updated_at | timestamptz | UpdatedTimestamp  |           |

### `public.external_chit_payloads`

| Column     | Type | Semantic  | FK Target |
| ---------- | ---- | --------- | --------- |
| user_id    | uuid |           |           |
| first_name | text |           |           |
| last_name  | text | Name      |           |
| email      | text | Email     |           |
| birthdate  | date | Birthdate |           |
| avatar     | text |           |           |
| city       | text | City      |           |
| state_abbr | text | State     |           |

### `public.f2_distribution_configs`

| Column                          | Type        | Semantic          | FK Target |
| ------------------------------- | ----------- | ----------------- | --------- |
| id                              | int4        | PK                |           |
| period_id                       | uuid        | Category          |           |
| period_name                     | text        | Category          |           |
| period_start                    | timestamptz | CreationTimestamp |           |
| period_end                      | timestamptz |                   |           |
| total_user_fly_throughput       | numeric     |                   |           |
| total_restaurant_fly_throughput | numeric     |                   |           |
| f2_user_allocation              | numeric     |                   |           |
| f2_restaurant_allocation        | numeric     |                   |           |
| excluded_location_ids           | \_text      |                   |           |
| claim_period_end_date           | timestamptz |                   |           |

### `public.f2_distributions`

| Column                     | Type        | Semantic          | FK Target |
| -------------------------- | ----------- | ----------------- | --------- |
| id                         | int4        | PK                |           |
| distribution_id            | uuid        |                   |           |
| created_at                 | timestamptz | CreationTimestamp |           |
| fly_throughput_snapshot_id | uuid        |                   |           |
| account_owner_type         | text        | Category          |           |
| account_owner_id           | uuid        | Owner             |           |
| distribution_amount        | numeric     |                   |           |
| period_id                  | uuid        | Category          |           |
| account_updated_at         | timestamptz | UpdatedTimestamp  |           |
| rank                       | int8        |                   |           |

### `public.failed_sessions`

| Column            | Type        | Semantic          | FK Target            |
| ----------------- | ----------- | ----------------- | -------------------- |
| id                | int4        | PK                |                      |
| failed_session_id | uuid        | Category          |                      |
| restaurant_id     | uuid        | Category          |                      |
| location_id       | uuid        | Category          |                      |
| nfc_chip_id       | uuid        |                   |                      |
| user_id           | uuid        | FK                | public.users.user_id |
| platform          | text        | Category          |                      |
| error_code        | text        | Category          |                      |
| reason            | text        | Category          |                      |
| debug_message     | text        | Category          |                      |
| created_at        | timestamptz | CreationTimestamp |                      |
| updated_at        | timestamptz | UpdatedTimestamp  |                      |

### `public.fly_airdrop_batches`

| Column         | Type        | Semantic          | FK Target |
| -------------- | ----------- | ----------------- | --------- |
| id             | uuid        | PK                |           |
| snapshot_id    | uuid        | Category          |           |
| transaction_id | uuid        | Category          |           |
| status         | text        | Category          |           |
| retry_count    | int4        | Quantity          |           |
| airdrop_amount | numeric     |                   |           |
| created_at     | timestamptz | CreationTimestamp |           |
| updated_at     | timestamptz | UpdatedTimestamp  |           |

### `public.fly_distribution_adjustments`

| Column                | Type        | Semantic          | FK Target |
| --------------------- | ----------- | ----------------- | --------- |
| id                    | int4        | PK                |           |
| date                  | date        |                   |           |
| days_remaining        | int4        |                   |           |
| projected_issuance    | numeric     |                   |           |
| actual_issuance       | numeric     |                   |           |
| created_at            | timestamptz | CreationTimestamp |           |
| updated_at            | timestamptz | UpdatedTimestamp  |           |
| total_future_issuance | numeric     |                   |           |

### `public.fly_ledger_entries`

| Column                 | Type        | Semantic          | FK Target                                          |
| ---------------------- | ----------- | ----------------- | -------------------------------------------------- |
| id                     | int4        | PK                |                                                    |
| fly_ledger_entry_id    | uuid        |                   |                                                    |
| origin_type            | text        | Category          |                                                    |
| origin_id              | uuid        |                   |                                                    |
| credit_amount          | numeric     |                   |                                                    |
| created_at             | timestamptz | CreationTimestamp |                                                    |
| updated_at             | timestamptz | UpdatedTimestamp  |                                                    |
| fly_multiplier         | int4        | Category          |                                                    |
| debit_amount           | numeric     |                   |                                                    |
| account_transaction_id | uuid        | FK                | public.account_transactions.account_transaction_id |
| account_balance_id     | uuid        | FK                | public.account_balances.account_balance_id         |
| balance_snapshot       | numeric     |                   |                                                    |

### `public.fly_purchase_requests`

| Column                  | Type        | Semantic          | FK Target |
| ----------------------- | ----------- | ----------------- | --------- |
| id                      | int4        | PK                |           |
| fly_purchase_request_id | uuid        | Category          |           |
| created_at              | timestamptz | CreationTimestamp |           |
| updated_at              | timestamptz | UpdatedTimestamp  |           |

### `public.fly_throughput_snapshots`

| Column                     | Type        | Semantic          | FK Target |
| -------------------------- | ----------- | ----------------- | --------- |
| id                         | int4        | PK                |           |
| fly_throughput_snapshot_id | uuid        |                   |           |
| created_at                 | timestamptz | CreationTimestamp |           |
| account_owner_type         | text        | Category          |           |
| account_owner_id           | uuid        | Owner             |           |
| account_updated_at         | timestamptz | UpdatedTimestamp  |           |
| account_balance            | numeric     |                   |           |
| debits                     | numeric     |                   |           |
| total_velocity             | numeric     |                   |           |
| period_id                  | uuid        | Category          |           |

### `public.flyway_schema_history`

| Column         | Type      | Semantic    | FK Target |
| -------------- | --------- | ----------- | --------- |
| installed_rank | int4      | PK          |           |
| version        | varchar   |             |           |
| description    | varchar   | Description |           |
| type           | varchar   | Category    |           |
| script         | varchar   |             |           |
| checksum       | int4      |             |           |
| installed_by   | varchar   | Category    |           |
| installed_on   | timestamp |             |           |
| execution_time | int4      |             |           |
| success        | bool      |             |           |

### `public.geography_columns`

| Column             | Type | Semantic | FK Target |
| ------------------ | ---- | -------- | --------- |
| f_table_catalog    | name |          |           |
| f_table_schema     | name |          |           |
| f_table_name       | name |          |           |
| f_geography_column | name |          |           |
| coord_dimension    | int4 |          |           |
| srid               | int4 |          |           |
| type               | text |          |           |

### `public.geometry_columns`

| Column            | Type    | Semantic | FK Target |
| ----------------- | ------- | -------- | --------- |
| f_table_catalog   | varchar | Category |           |
| f_table_schema    | name    | Category |           |
| f_table_name      | name    | Category |           |
| f_geometry_column | name    | Category |           |
| coord_dimension   | int4    | Category |           |
| srid              | int4    | Category |           |
| type              | varchar | Category |           |

### `public.guest_book_entries`

| Column        | Type        | Semantic          | FK Target                        |
| ------------- | ----------- | ----------------- | -------------------------------- |
| id            | int4        | PK                |                                  |
| restaurant_id | uuid        | FK                | public.restaurants.restaurant_id |
| user_id       | uuid        | FK                | public.users.user_id             |
| phone_number  | text        |                   |                                  |
| visits        | int4        | Category          |                                  |
| guest_notes   | text        | Category          |                                  |
| vip           | bool        |                   |                                  |
| created_at    | timestamptz | CreationTimestamp |                                  |
| updated_at    | timestamptz | UpdatedTimestamp  |                                  |

### `public.image_urls`

| Column     | Type        | Semantic | FK Target |
| ---------- | ----------- | -------- | --------- |
| id         | int4        | PK       |           |
| url        | text        |          |           |
| created_at | timestamptz |          |           |
| updated_at | timestamptz |          |           |

### `public.incentive_reads`

| Column       | Type      | Semantic          | FK Target            |
| ------------ | --------- | ----------------- | -------------------- |
| user_id      | uuid      | FK                | public.users.user_id |
| last_read_at | timestamp |                   |                      |
| updated_at   | timestamp | UpdatedTimestamp  |                      |
| created_at   | timestamp | CreationTimestamp |                      |

### `public.incentives`

| Column                                         | Type      | Semantic          | FK Target |
| ---------------------------------------------- | --------- | ----------------- | --------- |
| id                                             | int4      | PK                |           |
| reward_configuration → statusReward → statusId | text      | Category          |           |
| threshold → dineThreshold                      | decimal   | Category          |           |
| threshold → minimumSpend                       | decimal   |                   |           |
| threshold → referralThreshold                  | decimal   | Category          |           |
| threshold → spendThreshold                     | decimal   | Category          |           |
| incentive_id                                   | uuid      | Category          |           |
| type                                           | text      | Category          |           |
| title                                          | text      | Title             |           |
| description                                    | text      | Description       |           |
| image                                          | text      | URL               |           |
| threshold                                      | jsonb     | SerializedJSON    |           |
| start_time                                     | timestamp | CreationTimestamp |           |
| end_time                                       | timestamp |                   |           |
| expiration_period                              | text      |                   |           |
| expiration_type                                | text      | Category          |           |
| eligible_cohorts                               | jsonb     | SerializedJSON    |           |
| fly_reward                                     | numeric   |                   |           |
| created_at                                     | timestamp | CreationTimestamp |           |
| updated_at                                     | timestamp | UpdatedTimestamp  |           |
| terms                                          | text      | SerializedJSON    |           |
| notification_title                             | text      | Title             |           |
| notification_body                              | text      |                   |           |
| notification_route_url                         | text      | URL               |           |
| in_app_message                                 | text      |                   |           |
| accepted_currencies                            | jsonb     | SerializedJSON    |           |
| eligible_location_ids                          | jsonb     | SerializedJSON    |           |
| reward_configuration                           | jsonb     | SerializedJSON    |           |
| eligibility                                    | text      |                   |           |
| rewards                                        | jsonb     | SerializedJSON    |           |
| eligible_restaurant_ids                        | jsonb     | SerializedJSON    |           |

### `public.internal_chit_payloads`

| Column             | Type    | Semantic | FK Target |
| ------------------ | ------- | -------- | --------- |
| user_id            | uuid    |          |           |
| first_name         | text    |          |           |
| last_name          | text    | Name     |           |
| tip_percentage     | text    |          |           |
| fsr_spender_label  | text    | Category |           |
| qsr_spender_label  | text    | Category |           |
| last_three_label   | text    |          |           |
| neighborhood_label | text    |          |           |
| frequency_label    | text    | Category |           |
| fly_balance_label  | text    | Category |           |
| avg_tip_pct_raw    | numeric |          |           |
| avg_fsr_spend      | numeric |          |           |
| avg_qsr_spend      | numeric |          |           |
| visits_per_week    | numeric |          |           |
| fly_balance        | numeric |          |           |
| city               | text    | City     |           |
| state_abbr         | text    |          |           |
| avatar             | text    |          |           |

### `public.internal_chit_payloads_mv`

| Column             | Type    | Semantic | FK Target |
| ------------------ | ------- | -------- | --------- |
| user_id            | uuid    |          |           |
| first_name         | text    |          |           |
| last_name          | text    | Name     |           |
| tip_percentage     | text    |          |           |
| fsr_spender_label  | text    | Category |           |
| qsr_spender_label  | text    | Category |           |
| last_three_label   | text    |          |           |
| neighborhood_label | text    |          |           |
| frequency_label    | text    | Category |           |
| fly_balance_label  | text    | Category |           |
| avg_tip_pct_raw    | numeric |          |           |
| avg_fsr_spend      | numeric |          |           |
| avg_qsr_spend      | numeric |          |           |
| visits_per_week    | numeric |          |           |
| fly_balance        | numeric |          |           |
| city               | text    | City     |           |
| state_abbr         | text    |          |           |
| avatar             | text    |          |           |

### `public.ipfs_snapshots`

| Column         | Type        | Semantic | FK Target |
| -------------- | ----------- | -------- | --------- |
| id             | int4        | PK       |           |
| pin_cid        | text        |          |           |
| transaction_id | uuid        |          |           |
| batch_cutoff   | timestamptz |          |           |

### `public.jobrunr_backgroundjobservers`

| Column                     | Type      | Semantic | FK Target |
| -------------------------- | --------- | -------- | --------- |
| id                         | bpchar    | PK       |           |
| workerpoolsize             | int4      | Category |           |
| pollintervalinseconds      | int4      | Category |           |
| firstheartbeat             | timestamp |          |           |
| lastheartbeat              | timestamp |          |           |
| running                    | int4      | Category |           |
| systemtotalmemory          | int8      | Category |           |
| systemfreememory           | int8      | Category |           |
| systemcpuload              | numeric   |          |           |
| processmaxmemory           | int8      | Category |           |
| processfreememory          | int8      | Category |           |
| processallocatedmemory     | int8      | Category |           |
| processcpuload             | numeric   |          |           |
| deletesucceededjobsafter   | varchar   | Category |           |
| permanentlydeletejobsafter | varchar   | Category |           |
| name                       | varchar   | Name     |           |

### `public.jobrunr_jobs`

| Column         | Type      | Semantic          | FK Target |
| -------------- | --------- | ----------------- | --------- |
| id             | bpchar    | PK                |           |
| version        | int4      | Category          |           |
| jobasjson      | text      | SerializedJSON    |           |
| jobsignature   | varchar   | Category          |           |
| state          | varchar   | Category          |           |
| createdat      | timestamp | CreationTimestamp |           |
| updatedat      | timestamp | UpdatedTimestamp  |           |
| scheduledat    | timestamp |                   |           |
| recurringjobid | varchar   | Category          |           |

### `public.jobrunr_jobs_stats`

| Column                    | Type    | Semantic | FK Target |
| ------------------------- | ------- | -------- | --------- |
| total                     | int8    |          |           |
| awaiting                  | int8    |          |           |
| scheduled                 | int8    |          |           |
| enqueued                  | int8    |          |           |
| processing                | int8    |          |           |
| failed                    | int8    |          |           |
| succeeded                 | int8    |          |           |
| alltimesucceeded          | numeric |          |           |
| deleted                   | int8    |          |           |
| nbrofbackgroundjobservers | int8    | Category |           |
| nbrofrecurringjobs        | int8    | Category |           |

### `public.jobrunr_metadata`

| Column    | Type      | Semantic          | FK Target |
| --------- | --------- | ----------------- | --------- |
| id        | varchar   | PK                |           |
| name      | varchar   | Name              |           |
| owner     | varchar   | Owner             |           |
| value     | text      | Category          |           |
| createdat | timestamp | CreationTimestamp |           |
| updatedat | timestamp | UpdatedTimestamp  |           |

### `public.jobrunr_migrations`

| Column      | Type    | Semantic | FK Target |
| ----------- | ------- | -------- | --------- |
| id          | bpchar  | PK       |           |
| script      | varchar | Category |           |
| installedon | varchar | Category |           |

### `public.jobrunr_recurring_jobs`

| Column    | Type   | Semantic       | FK Target |
| --------- | ------ | -------------- | --------- |
| id        | bpchar | PK             |           |
| version   | int4   | Category       |           |
| jobasjson | text   | SerializedJSON |           |
| createdat | int8   | Category       |           |

### `public.launch_info`

| Column               | Type        | Semantic          | FK Target |
| -------------------- | ----------- | ----------------- | --------- |
| id                   | int4        | PK                |           |
| platform             | text        | Category          |           |
| app_name             | text        | Category          |           |
| minimum_app_version  | text        | Category          |           |
| current_app_version  | text        | Category          |           |
| created_at           | timestamptz | CreationTimestamp |           |
| updated_at           | timestamptz | UpdatedTimestamp  |           |
| latest_terms_version | date        |                   |           |

### `public.location_ai_data`

| Column            | Type      | Semantic          | FK Target                    |
| ----------------- | --------- | ----------------- | ---------------------------- |
| location_id       | uuid      | FK                | public.locations.location_id |
| recommended_items | \_text    |                   |                              |
| description       | text      | Description       |                              |
| created_at        | timestamp | CreationTimestamp |                              |
| updated_at        | timestamp | UpdatedTimestamp  |                              |
| what_to_know      | \_text    |                   |                              |
| restaurant_id     | varchar   |                   |                              |
| reservation_url   | varchar   | URL               |                              |
| instagram_url     | varchar   | URL               |                              |

### `public.location_summaries`

| Column           | Type        | Semantic          | FK Target                            |
| ---------------- | ----------- | ----------------- | ------------------------------------ |
| id               | int4        | PK                |                                      |
| date             | date        |                   |                                      |
| neighborhood_id  | uuid        | FK                | public.neighborhoods.neighborhood_id |
| live             | int4        | Category          |                                      |
| payments_enabled | int4        | Category          |                                      |
| created_at       | timestamptz | CreationTimestamp |                                      |
| updated_at       | timestamptz | UpdatedTimestamp  |                                      |

### `public.location_weekly_reports`

| Column                                 | Type    | Semantic       | FK Target |
| -------------------------------------- | ------- | -------------- | --------- |
| check_in_summary → last_week           | decimal |                |           |
| check_in_summary → repeat              | decimal |                |           |
| check_in_summary → this_week           | decimal |                |           |
| location_id                            | uuid    |                |           |
| membership_summary → last_week         | decimal |                |           |
| membership_summary → this_week         | decimal |                |           |
| payment_volume_summary → last_week     | decimal |                |           |
| payment_volume_summary → this_week     | decimal |                |           |
| payment_volume_summary → total_savings | decimal |                |           |
| restaurant_id                          | uuid    |                |           |
| location_name                          | text    |                |           |
| restaurant_name                        | text    |                |           |
| two_weeks_ago                          | date    |                |           |
| one_week_ago                           | date    |                |           |
| today                                  | date    |                |           |
| membership_summary                     | json    | SerializedJSON |           |
| check_in_summary                       | json    | SerializedJSON |           |
| payment_volume_summary                 | json    | SerializedJSON |           |
| top_user_ids                           | \_uuid  |                |           |

### `public.locations`

| Column                                     | Type        | Semantic          | FK Target                                 |
| ------------------------------------------ | ----------- | ----------------- | ----------------------------------------- |
| id                                         | int4        | PK                |                                           |
| location_id                                | uuid        |                   |                                           |
| restaurant_id                              | uuid        | FK                | public.restaurants.restaurant_id          |
| name                                       | text        | Name              |                                           |
| messaging_country_code                     | text        | Category          |                                           |
| messaging_phone_number                     | text        |                   |                                           |
| street                                     | text        |                   |                                           |
| street2                                    | text        | Category          |                                           |
| city                                       | text        | City              |                                           |
| state                                      | text        | State             |                                           |
| zipcode                                    | text        | ZipCode           |                                           |
| country                                    | text        | Country           |                                           |
| created_at                                 | timestamptz | CreationTimestamp |                                           |
| updated_at                                 | timestamptz | UpdatedTimestamp  |                                           |
| wifi_ssid                                  | text        | Category          |                                           |
| wifi_password                              | text        | Category          |                                           |
| time_zone                                  | text        | Category          |                                           |
| coordinate                                 | geometry    |                   |                                           |
| rooam_pos_id                               | uuid        |                   |                                           |
| payments_enabled                           | bool        |                   |                                           |
| opentable_id                               | text        | Category          |                                           |
| opentable_external_id                      | uuid        | Category          |                                           |
| neighborhood_id                            | uuid        | FK                | public.neighborhoods.neighborhood_id      |
| reservation_url                            | text        | URL               |                                           |
| live                                       | bool        |                   |                                           |
| google_place_id                            | text        |                   |                                           |
| open_hours_last_synced_at                  | timestamptz |                   |                                           |
| open_hours_override                        | bool        |                   |                                           |
| is_billable                                | bool        |                   |                                           |
| accepts_prepayment                         | bool        |                   |                                           |
| requires_employee_pin                      | bool        |                   |                                           |
| sandbox_enabled_at                         | timestamptz |                   |                                           |
| square_merchant_id                         | text        |                   |                                           |
| square_token_id                            | uuid        | FK                | square.tokens.token_id                    |
| blackbird_fee_bips                         | int4        |                   |                                           |
| use_square_sidecar                         | bool        |                   |                                           |
| resy_token_id                              | uuid        | FK                |                                           |
| resy_venue_id                              | int4        |                   |                                           |
| is_club                                    | bool        |                   |                                           |
| service_charge_bips                        | int4        | Category          |                                           |
| google_maps_rating                         | float8      | Score             |                                           |
| create_landing_page                        | bool        |                   |                                           |
| service_charge_frequency                   | text        | Category          |                                           |
| sidecar_configurable                       | bool        |                   |                                           |
| auto_gratuity_enabled                      | bool        |                   |                                           |
| pos_type                                   | text        | Category          |                                           |
| slug                                       | text        |                   |                                           |
| employee_incentive_cadence                 | text        | Category          |                                           |
| employee_incentive_target                  | int4        |                   |                                           |
| has_sidecar_table_number                   | bool        |                   |                                           |
| has_sidecar_check_number                   | bool        |                   |                                           |
| employee_incentive_group_reward_cents      | int4        |                   |                                           |
| employee_incentive_individual_reward_cents | int4        |                   |                                           |
| square_location_id                         | text        |                   |                                           |
| supergood_toast_credential_id              | uuid        | FK                | supergood_toast.credentials.credential_id |

### `public.locations_aud`

| Column           | Type        | Semantic          | FK Target          |
| ---------------- | ----------- | ----------------- | ------------------ |
| id               | int4        | PK                |                    |
| rev              | int4        | FK                | public.revinfo.rev |
| revtype          | int2        | Category          |                    |
| payments_enabled | bool        |                   |                    |
| created_at       | timestamptz | CreationTimestamp |                    |
| coordinate       | geometry    |                   |                    |

### `public.locations_updates`

| Column                | Type        | Semantic | FK Target |
| --------------------- | ----------- | -------- | --------- |
| location_id           | uuid        |          |           |
| id                    | int4        | PK       |           |
| last_payments_enabled | timestamptz |          |           |
| last_coordinate       | timestamptz |          |           |

### `public.media`

| Column         | Type        | Semantic          | FK Target                        |
| -------------- | ----------- | ----------------- | -------------------------------- |
| id             | int4        | PK                |                                  |
| media_id       | uuid        |                   |                                  |
| restaurant_id  | uuid        | FK                | public.restaurants.restaurant_id |
| file_type      | text        | Category          |                                  |
| title          | text        | Title             |                                  |
| url            | text        | URL               |                                  |
| created_at     | timestamptz | CreationTimestamp |                                  |
| updated_at     | timestamptz | UpdatedTimestamp  |                                  |
| file_extension | text        | Category          |                                  |

### `public.media_promotions`

| Column             | Type        | Semantic          | FK Target             |
| ------------------ | ----------- | ----------------- | --------------------- |
| id                 | int4        | PK                |                       |
| media_promotion_id | uuid        | PK                |                       |
| media_id           | uuid        | FK                | public.media.media_id |
| start_date_time    | timestamptz | CreationTimestamp |                       |
| end_date_time      | timestamptz |                   |                       |
| created_at         | timestamptz | CreationTimestamp |                       |
| updated_at         | timestamptz | UpdatedTimestamp  |                       |

### `public.membership_events`

| Column             | Type        | Semantic          | FK Target                                  |
| ------------------ | ----------- | ----------------- | ------------------------------------------ |
| id                 | int4        | PK                |                                            |
| membership_id      | uuid        | FK                | public.memberships.membership_id           |
| membership_tier_id | uuid        | FK                | public.membership_tiers.membership_tier_id |
| event_type         | text        | Category          |                                            |
| event_source       | text        | Source            |                                            |
| event_source_id    | uuid        | Source            |                                            |
| created_at         | timestamptz | CreationTimestamp |                                            |
| updated_at         | timestamptz | UpdatedTimestamp  |                                            |

### `public.membership_tiers`

| Column                         | Type        | Semantic          | FK Target |
| ------------------------------ | ----------- | ----------------- | --------- |
| id                             | int4        | PK                |           |
| membership_tier_id             | uuid        |                   |           |
| access_level                   | int4        | Category          |           |
| name                           | text        | Name              |           |
| active                         | bool        |                   |           |
| created_at                     | timestamptz | CreationTimestamp |           |
| updated_at                     | timestamptz | UpdatedTimestamp  |           |
| quantity                       | int4        | Quantity          |           |
| term_value                     | int4        | Category          |           |
| term_unit                      | text        | Category          |           |
| artist                         | text        | Category          |           |
| image                          | text        | URL               |           |
| restaurant_id                  | uuid        |                   |           |
| renewable                      | bool        |                   |           |
| about_copy                     | text        |                   |           |
| how_it_works_copy              | text        |                   |           |
| benefits_copy                  | text        |                   |           |
| messaging_enabled              | bool        |                   |           |
| quantity_remaining             | int4        | Quantity          |           |
| confirmation_email_copy        | text        |                   |           |
| confirmation_email_header_copy | text        |                   |           |
| price_usd                      | int8        | Category          |           |
| image_preview                  | text        | URL               |           |
| image_full                     | text        | URL               |           |
| image_web                      | text        | URL               |           |

### `public.memberships`

| Column                | Type        | Semantic          | FK Target                                  |
| --------------------- | ----------- | ----------------- | ------------------------------------------ |
| id                    | int4        | PK                |                                            |
| membership_id         | uuid        |                   |                                            |
| user_id               | uuid        | FK                | public.users.user_id                       |
| nft_id                | uuid        | FK                | public.nfts.nft_id                         |
| acquisition_source    | text        | Source            |                                            |
| acquisition_source_id | uuid        | Source            |                                            |
| status                | text        | Category          |                                            |
| created_at            | timestamptz | CreationTimestamp |                                            |
| updated_at            | timestamptz | UpdatedTimestamp  |                                            |
| membership_tier_id    | uuid        | FK                | public.membership_tiers.membership_tier_id |
| restaurant_id         | uuid        | FK                | public.restaurants.restaurant_id           |
| total_fly             | numeric     |                   |                                            |
| check_in_count        | int4        | Quantity          |                                            |
| last_check_in_date    | timestamptz |                   |                                            |
| referral_count        | int4        | Quantity          |                                            |
| messaging_enabled     | bool        |                   |                                            |

### `public.menu_option_sets`

| Column             | Type        | Semantic          | FK Target |
| ------------------ | ----------- | ----------------- | --------- |
| id                 | int4        | PK                |           |
| menu_option_set_id | uuid        |                   |           |
| name               | text        | Name              |           |
| minimum_selections | int4        | Category          |           |
| required           | bool        |                   |           |
| created_at         | timestamptz | CreationTimestamp |           |
| updated_at         | timestamptz | UpdatedTimestamp  |           |
| version            | int8        | Category          |           |

### `public.neighborhood_zipcodes`

| Column                   | Type      | Semantic          | FK Target |
| ------------------------ | --------- | ----------------- | --------- |
| id                       | int4      | PK                |           |
| neighborhood_name        | text      |                   |           |
| zipcode_int              | text      |                   |           |
| created_at               | timestamp | CreationTimestamp |           |
| updated_at               | timestamp | UpdatedTimestamp  |           |
| zipcode                  | text      | ZipCode           |           |
| city                     | text      | City              |           |
| state_abbr               | text      | State             |           |
| state_name               | text      | State             |           |
| zcta                     | bool      |                   |           |
| zcta_parent              | text      |                   |           |
| population               | int4      |                   |           |
| density                  | numeric   |                   |           |
| county_code_primary      | text      |                   |           |
| county_name              | text      |                   |           |
| county_weights           | jsonb     | SerializedJSON    |           |
| official_county_names    | text      |                   |           |
| official_county_code     | text      |                   |           |
| imprecise                | bool      |                   |           |
| military                 | bool      |                   |           |
| time_zone                | text      | Category          |           |
| geo_point                | geometry  |                   |           |
| latitude                 | numeric   | Latitude          |           |
| longitude                | numeric   | Longitude         |           |
| country_code             | varchar   | Country           |           |
| households_200k_plus_pct | numeric   |                   |           |
| housing_units            | int4      |                   |           |
| households               | int4      |                   |           |
| avg_income               | int4      | Income            |           |
| median_income            | int4      | Income            |           |

### `public.neighborhoods`

| Column          | Type        | Semantic          | FK Target |
| --------------- | ----------- | ----------------- | --------- |
| id              | int4        | PK                |           |
| neighborhood_id | uuid        |                   |           |
| name            | text        | Name              |           |
| city            | text        | City              |           |
| created_at      | timestamptz | CreationTimestamp |           |
| updated_at      | timestamptz | UpdatedTimestamp  |           |

### `public.nfc_chips`

| Column        | Type        | Semantic          | FK Target                        |
| ------------- | ----------- | ----------------- | -------------------------------- |
| id            | int4        | PK                |                                  |
| nfc_chip_id   | uuid        |                   |                                  |
| restaurant_id | uuid        | FK                | public.restaurants.restaurant_id |
| action        | text        | Category          |                                  |
| created_at    | timestamptz | CreationTimestamp |                                  |
| updated_at    | timestamptz | UpdatedTimestamp  |                                  |
| table_number  | text        |                   |                                  |
| location_id   | uuid        |                   |                                  |
| read_ctr      | numeric     |                   |                                  |

### `public.nft_airdrop_batches`

| Column               | Type        | Semantic          | FK Target |
| -------------------- | ----------- | ----------------- | --------- |
| id                   | int4        | PK                |           |
| nft_airdrop_batch_id | uuid        |                   |           |
| transaction_id       | uuid        |                   |           |
| status               | text        | Category          |           |
| quantity_airdropped  | int4        | Quantity          |           |
| created_at           | timestamptz | CreationTimestamp |           |
| updated_at           | timestamptz | UpdatedTimestamp  |           |

### `public.nft_mint_batches`

| Column               | Type        | Semantic          | FK Target |
| -------------------- | ----------- | ----------------- | --------- |
| id                   | uuid        | PK                |           |
| created_at           | timestamptz | CreationTimestamp |           |
| updated_at           | timestamptz | UpdatedTimestamp  |           |
| transaction_id       | uuid        |                   |           |
| nft_contract_address | text        | Category          |           |
| status               | text        | Category          |           |
| starting_token_id    | numeric     |                   |           |
| quantity_minted      | int4        | Quantity          |           |

### `public.nft_supply_counts`

| Column           | Type    | Semantic | FK Target |
| ---------------- | ------- | -------- | --------- |
| id               | int4    | PK       |           |
| contract_address | text    | Category |           |
| total_minted     | numeric |          |           |

### `public.nfts`

| Column               | Type        | Semantic          | FK Target                                       |
| -------------------- | ----------- | ----------------- | ----------------------------------------------- |
| id                   | int4        | PK                |                                                 |
| nft_id               | uuid        |                   |                                                 |
| created_at           | timestamptz | CreationTimestamp |                                                 |
| updated_at           | timestamptz | UpdatedTimestamp  |                                                 |
| token_id             | numeric     |                   |                                                 |
| owner_address        | text        | Owner             |                                                 |
| owner_user_id        | uuid        | FK                | public.users.user_id                            |
| metadata_url         | text        | URL               |                                                 |
| status               | text        | Category          |                                                 |
| restaurant_id        | uuid        | FK                | public.restaurants.restaurant_id                |
| contract_address     | text        | Category          |                                                 |
| nft_airdrop_batch_id | uuid        | FK                | public.nft_airdrop_batches.nft_airdrop_batch_id |

### `public.open_hours`

| Column      | Type        | Semantic          | FK Target                    |
| ----------- | ----------- | ----------------- | ---------------------------- |
| id          | int4        | PK                |                              |
| location_id | uuid        | FK                | public.locations.location_id |
| day_of_week | text        | Category          |                              |
| start_time  | time        | CreationTime      |                              |
| end_time    | time        |                   |                              |
| created_at  | timestamptz | CreationTimestamp |                              |
| updated_at  | timestamptz | UpdatedTimestamp  |                              |

### `public.opentable_guests`

| Column         | Type      | Semantic          | FK Target                    |
| -------------- | --------- | ----------------- | ---------------------------- |
| id             | int4      | PK                |                              |
| user_id        | uuid      | FK                | public.users.user_id         |
| location_id    | uuid      | FK                | public.locations.location_id |
| venue_guest_id | text      | Category          |                              |
| created_at     | timestamp | CreationTimestamp |                              |
| updated_at     | timestamp | UpdatedTimestamp  |                              |

### `public.passes`

| Column                | Type        | Semantic          | FK Target                              |
| --------------------- | ----------- | ----------------- | -------------------------------------- |
| id                    | int4        | PK                |                                        |
| pass_id               | uuid        |                   |                                        |
| user_id               | uuid        | FK                | public.users.user_id                   |
| collaboration_id      | uuid        | FK                | public.collaborations.collaboration_id |
| nft_id                | uuid        | FK                | public.nfts.nft_id                     |
| acquisition_source    | text        | Source            |                                        |
| acquisition_source_id | uuid        | Source            |                                        |
| created_at            | timestamptz | CreationTimestamp |                                        |
| updated_at            | timestamptz | UpdatedTimestamp  |                                        |
| state                 | text        | Category          |                                        |
| expires_at            | timestamptz |                   |                                        |
| visit_count           | int4        | Quantity          |                                        |
| restaurants_visited   | int4        | Category          |                                        |
| auto_renew            | bool        |                   |                                        |

### `public.passes_aud`

| Column     | Type | Semantic | FK Target          |
| ---------- | ---- | -------- | ------------------ |
| id         | int4 | PK       |                    |
| rev        | int4 | FK       | public.revinfo.rev |
| revtype    | int2 | Category |                    |
| state      | text | Category |                    |
| auto_renew | bool |          |                    |

### `public.pay_settings`

| Column                   | Type      | Semantic          | FK Target            |
| ------------------------ | --------- | ----------------- | -------------------- |
| id                       | int4      | PK                |                      |
| user_id                  | uuid      | FK                | public.users.user_id |
| default_tip_percent      | int4      |                   |                      |
| default_pay_with_fly     | bool      |                   |                      |
| hide_check_settings_page | bool      |                   |                      |
| created_at               | timestamp | CreationTimestamp |                      |
| updated_at               | timestamp | UpdatedTimestamp  |                      |

### `public.payment_links`

| Column                   | Type        | Semantic          | FK Target                                  |
| ------------------------ | ----------- | ----------------- | ------------------------------------------ |
| id                       | int4        | PK                |                                            |
| payment_link_id          | uuid        | Category          |                                            |
| payee_account_balance_id | uuid        | FK                | public.account_balances.account_balance_id |
| amount_cents             | int8        |                   |                                            |
| description              | text        | Description       |                                            |
| expires_at               | timestamptz |                   |                                            |
| created_at               | timestamptz | CreationTimestamp |                                            |
| updated_at               | timestamptz | UpdatedTimestamp  |                                            |
| paid_at                  | timestamptz |                   |                                            |

### `public.payments`

| Column                 | Type        | Semantic          | FK Target                  |
| ---------------------- | ----------- | ----------------- | -------------------------- |
| id                     | int4        | PK                |                            |
| payment_id             | uuid        |                   |                            |
| external_id            | text        |                   |                            |
| user_id                | uuid        | FK                | public.users.user_id       |
| provider               | text        | Category          |                            |
| currency               | text        | Category          |                            |
| amount                 | int8        |                   |                            |
| status                 | text        | Category          |                            |
| created_at             | timestamptz | CreationTimestamp |                            |
| updated_at             | timestamptz | UpdatedTimestamp  |                            |
| item_type              | text        | Category          |                            |
| item_id                | uuid        |                   |                            |
| original_payment_id    | uuid        | FK                | public.payments.payment_id |
| payment_method_type    | text        | Category          |                            |
| payment_method_id      | uuid        |                   |                            |
| provider_response_code | text        |                   |                            |
| refund_amount          | int8        | Category          |                            |

### `public.payout_accounts`

| Column            | Type        | Semantic          | FK Target                        |
| ----------------- | ----------- | ----------------- | -------------------------------- |
| id                | int4        | PK                |                                  |
| payout_account_id | uuid        | Category          |                                  |
| provider          | text        | Category          |                                  |
| provider_id       | text        | Category          |                                  |
| restaurant_id     | uuid        | FK                | public.restaurants.restaurant_id |
| created_at        | timestamptz | CreationTimestamp |                                  |
| updated_at        | timestamptz | UpdatedTimestamp  |                                  |
| location_id       | uuid        | Category          |                                  |

### `public.payouts`

| Column                    | Type        | Semantic          | FK Target                                |
| ------------------------- | ----------- | ----------------- | ---------------------------------------- |
| id                        | int4        | PK                |                                          |
| payout_id                 | uuid        |                   |                                          |
| period_end_time           | timestamptz |                   |                                          |
| status                    | text        | Category          |                                          |
| total_check_amount        | int8        |                   |                                          |
| bb_fee_bips               | int8        | Category          |                                          |
| bb_fee_amount             | int8        |                   |                                          |
| net_payout_amount         | int8        |                   |                                          |
| restaurant_id             | uuid        | FK                | public.restaurants.restaurant_id         |
| payout_account_id         | uuid        | FK                | public.payout_accounts.payout_account_id |
| created_at                | timestamptz | CreationTimestamp |                                          |
| updated_at                | timestamptz | UpdatedTimestamp  |                                          |
| location_id               | uuid        | Category          |                                          |
| provider_id               | text        |                   |                                          |
| total_adjustment_amount   | int8        |                   |                                          |
| total_due_amount          | int8        |                   |                                          |
| external_bill_id          | varchar     |                   |                                          |
| bb_transaction_fee_amount | int8        | Category          |                                          |

### `public.pg_stat_statements`

| Column              | Type    | Semantic | FK Target |
| ------------------- | ------- | -------- | --------- |
| userid              | oid     |          |           |
| dbid                | oid     |          |           |
| toplevel            | bool    |          |           |
| queryid             | int8    |          |           |
| query               | text    |          |           |
| plans               | int8    | Category |           |
| total_plan_time     | float8  |          |           |
| min_plan_time       | float8  |          |           |
| max_plan_time       | float8  |          |           |
| mean_plan_time      | float8  |          |           |
| stddev_plan_time    | float8  |          |           |
| calls               | int8    |          |           |
| total_exec_time     | float8  |          |           |
| min_exec_time       | float8  |          |           |
| max_exec_time       | float8  |          |           |
| mean_exec_time      | float8  |          |           |
| stddev_exec_time    | float8  |          |           |
| rows                | int8    |          |           |
| shared_blks_hit     | int8    |          |           |
| shared_blks_read    | int8    |          |           |
| shared_blks_dirtied | int8    | Category |           |
| shared_blks_written | int8    | Category |           |
| local_blks_hit      | int8    | Category |           |
| local_blks_read     | int8    | Category |           |
| local_blks_dirtied  | int8    | Category |           |
| local_blks_written  | int8    | Category |           |
| temp_blks_read      | int8    |          |           |
| temp_blks_written   | int8    |          |           |
| blk_read_time       | float8  |          |           |
| blk_write_time      | float8  |          |           |
| wal_records         | int8    | Category |           |
| wal_fpi             | int8    | Category |           |
| wal_bytes           | numeric |          |           |

### `public.pg_stat_statements_info`

| Column      | Type        | Semantic | FK Target |
| ----------- | ----------- | -------- | --------- |
| dealloc     | int8        | Category |           |
| stats_reset | timestamptz |          |           |

### `public.popular_restaurants_view`

| Column        | Type | Semantic | FK Target |
| ------------- | ---- | -------- | --------- |
| id            | int8 | PK       |           |
| region_id     | uuid | Category |           |
| restaurant_id | uuid |          |           |
| name          | text | Name     |           |
| score         | int4 | Score    |           |
| cohort        | text | Category |           |
| is_bb1        | bool |          |           |

### `public.ppx_entries`

| Column             | Type        | Semantic          | FK Target                                  |
| ------------------ | ----------- | ----------------- | ------------------------------------------ |
| id                 | int4        | PK                |                                            |
| ppx_entry_id       | uuid        |                   |                                            |
| restaurant_id      | uuid        | Category          |                                            |
| membership_tier_id | uuid        | FK                | public.membership_tiers.membership_tier_id |
| phone_number       | text        |                   |                                            |
| email              | text        |                   |                                            |
| full_name          | text        | Name              |                                            |
| created_at         | timestamptz | CreationTimestamp |                                            |
| updated_at         | timestamptz | UpdatedTimestamp  |                                            |

### `public.press_checks_backup`

| Column     | Type        | Semantic          | FK Target |
| ---------- | ----------- | ----------------- | --------- |
| check_id   | uuid        |                   |           |
| created_at | timestamptz | CreationTimestamp |           |

### `public.private_dining_rooms`

| Column                    | Type        | Semantic          | FK Target                                  |
| ------------------------- | ----------- | ----------------- | ------------------------------------------ |
| id                        | int8        | PK                |                                            |
| pdr_id                    | uuid        | Category          |                                            |
| location_id               | uuid        | FK                | public.locations.location_id               |
| restaurant_user_id        | uuid        | FK                | public.restaurant_users.restaurant_user_id |
| customer_email            | varchar     | Email             |                                            |
| event_description         | text        | Description       |                                            |
| deposit_amount_cents      | int8        |                   |                                            |
| final_charge_amount_cents | int8        |                   |                                            |
| status                    | text        | Category          |                                            |
| payment_link_id           | uuid        | FK                | public.payment_links.payment_link_id       |
| card_id                   | uuid        | FK                | public.cards.card_id                       |
| requires_card_on_file     | bool        |                   |                                            |
| deposit_paid_at           | timestamptz |                   |                                            |
| final_charge_processed_at | timestamptz |                   |                                            |
| created_at                | timestamptz | CreationTimestamp |                                            |
| updated_at                | timestamptz | UpdatedTimestamp  |                                            |
| event_date                | timestamptz |                   |                                            |

### `public.promo_codes`

| Column         | Type      | Semantic          | FK Target |
| -------------- | --------- | ----------------- | --------- |
| id             | int4      | PK                |           |
| promo_code_id  | uuid      | Category          |           |
| product_type   | text      | Category          |           |
| product_id     | uuid      | Category          |           |
| discount_type  | text      | Category          |           |
| discount_value | int8      | Discount          |           |
| code           | varchar   | Category          |           |
| active         | bool      |                   |           |
| created_at     | timestamp | CreationTimestamp |           |
| updated_at     | timestamp | UpdatedTimestamp  |           |

### `public.promotion_applications`

| Column                   | Type        | Semantic          | FK Target                                            |
| ------------------------ | ----------- | ----------------- | ---------------------------------------------------- |
| id                       | int4        | PK                |                                                      |
| promotion_application_id | uuid        | Category          |                                                      |
| promotion_redemption_id  | uuid        | FK                | public.promotion_redemptions.promotion_redemption_id |
| item_id                  | uuid        | Category          |                                                      |
| item_type                | text        | Category          |                                                      |
| created_at               | timestamptz | CreationTimestamp |                                                      |
| updated_at               | timestamptz | UpdatedTimestamp  |                                                      |

### `public.promotion_codes`

| Column                | Type        | Semantic          | FK Target                |
| --------------------- | ----------- | ----------------- | ------------------------ |
| id                    | int4        | PK                |                          |
| promotion_code_id     | uuid        | Category          |                          |
| active                | bool        |                   |                          |
| code                  | varchar     | Category          |                          |
| expires_at            | timestamptz |                   |                          |
| max_redemptions       | int4        | Category          |                          |
| times_redeemed        | int4        | Category          |                          |
| coupon_id             | uuid        | FK                | public.coupons.coupon_id |
| created_at            | timestamptz | CreationTimestamp |                          |
| updated_at            | timestamptz | UpdatedTimestamp  |                          |
| user_id               | uuid        | FK                | public.users.user_id     |
| acquisition_source    | text        | Source            |                          |
| acquisition_source_id | uuid        | Source            |                          |

### `public.promotion_redemptions`

| Column                  | Type        | Semantic          | FK Target                                |
| ----------------------- | ----------- | ----------------- | ---------------------------------------- |
| id                      | int4        | PK                |                                          |
| promotion_redemption_id | uuid        | Category          |                                          |
| starts_at               | timestamptz | CreationTimestamp |                                          |
| ends_at                 | timestamptz |                   |                                          |
| promotion_code_id       | uuid        | FK                | public.promotion_codes.promotion_code_id |
| user_id                 | uuid        | FK                | public.users.user_id                     |
| created_at              | timestamptz | CreationTimestamp |                                          |
| updated_at              | timestamptz | UpdatedTimestamp  |                                          |

### `public.ranked_fly_throughput_view`

| Column               | Type        | Semantic         | FK Target |
| -------------------- | ----------- | ---------------- | --------- |
| account_owner_type   | text        | Category         |           |
| account_owner_id     | uuid        | Owner            |           |
| account_updated_at   | timestamptz | UpdatedTimestamp |           |
| account_balance      | numeric     |                  |           |
| debits               | numeric     |                  |           |
| total_velocity       | numeric     |                  |           |
| rank                 | int8        |                  |           |
| account_balance_id   | int4        |                  |           |
| account_balance_uuid | uuid        |                  |           |
| period_id            | uuid        | Category         |           |

### `public.referral_codes`

| Column                   | Type        | Semantic          | FK Target                          |
| ------------------------ | ----------- | ----------------- | ---------------------------------- |
| id                       | int4        | PK                |                                    |
| code                     | text        |                   |                                    |
| user_id                  | uuid        | FK                | public.users.user_id               |
| restaurant_id            | uuid        | FK                | public.restaurants.restaurant_id   |
| active                   | bool        |                   |                                    |
| created_at               | timestamptz | CreationTimestamp |                                    |
| updated_at               | timestamptz | UpdatedTimestamp  |                                    |
| recipient_reward_rule_id | uuid        | FK                | public.reward_rules.reward_rule_id |
| sender_reward_usd        | int8        |                   |                                    |
| sender_alias             | text        |                   |                                    |

### `public.referrals`

| Column            | Type        | Semantic          | FK Target                        |
| ----------------- | ----------- | ----------------- | -------------------------------- |
| id                | int4        | PK                |                                  |
| referral_id       | uuid        |                   |                                  |
| sender_user_id    | uuid        | FK                | public.users.user_id             |
| recipient_user_id | uuid        | FK                | public.users.user_id             |
| restaurant_id     | uuid        | FK                | public.restaurants.restaurant_id |
| code              | text        | FK                | public.referral_codes.code       |
| state             | text        | Category          |                                  |
| created_at        | timestamptz | CreationTimestamp |                                  |
| updated_at        | timestamptz | UpdatedTimestamp  |                                  |

### `public.refunds`

| Column               | Type        | Semantic          | FK Target                          |
| -------------------- | ----------- | ----------------- | ---------------------------------- |
| id                   | int4        | PK                |                                    |
| refund_id            | uuid        | Category          |                                    |
| amount               | int8        | Category          |                                    |
| currency             | text        | Category          |                                    |
| check_share_id       | uuid        | FK                | public.check_shares.check_share_id |
| refund_reason        | text        | Category          |                                    |
| comment              | text        | Comment           |                                    |
| refund_status        | text        | Category          |                                    |
| external_id          | text        |                   |                                    |
| provider             | text        |                   |                                    |
| payout_id            | uuid        | FK                | public.payouts.payout_id           |
| created_at           | timestamptz | CreationTimestamp |                                    |
| updated_at           | timestamptz | UpdatedTimestamp  |                                    |
| fly_amount           | int8        | Category          |                                    |
| house_account_amount | int8        | Category          |                                    |
| usd_amount           | int8        | Category          |                                    |

### `public.regions`

| Column     | Type        | Semantic          | FK Target |
| ---------- | ----------- | ----------------- | --------- |
| id         | int4        | PK                |           |
| region_id  | uuid        | Category          |           |
| name       | text        | Name              |           |
| center     | geometry    | Category          |           |
| radius     | float8      |                   |           |
| active     | bool        |                   |           |
| created_at | timestamptz | CreationTimestamp |           |
| updated_at | timestamptz | UpdatedTimestamp  |           |
| time_zone  | text        | Category          |           |

### `public.reservation_requests`

| Column                 | Type        | Semantic          | FK Target                          |
| ---------------------- | ----------- | ----------------- | ---------------------------------- |
| id                     | int4        | PK                |                                    |
| reservation_request_id | uuid        | Category          |                                    |
| user_id                | uuid        | FK                | public.users.user_id               |
| location_id            | uuid        | FK                | public.locations.location_id       |
| reservation_id         | uuid        | FK                | public.reservations.reservation_id |
| state                  | text        | Category          |                                    |
| party_size             | int4        | Category          |                                    |
| request_dates          | jsonb       | SerializedJSON    |                                    |
| request_start_time     | time        | CreationTime      |                                    |
| request_end_time       | time        |                   |                                    |
| created_at             | timestamptz | CreationTimestamp |                                    |
| updated_at             | timestamptz | UpdatedTimestamp  |                                    |
| platform               | text        | Category          |                                    |

### `public.reservations`

| Column              | Type        | Semantic          | FK Target                    |
| ------------------- | ----------- | ----------------- | ---------------------------- |
| id                  | int4        | PK                |                              |
| provider_type       | text        | Category          |                              |
| user_id             | uuid        | FK                | public.users.user_id         |
| location_id         | uuid        | FK                | public.locations.location_id |
| server_name         | text        |                   |                              |
| table_number        | text        | Category          |                              |
| party_size          | int4        | Category          |                              |
| reservation_time    | timestamptz |                   |                              |
| external_id         | text        | Category          |                              |
| state               | text        | Category          |                              |
| created_at          | timestamptz | CreationTimestamp |                              |
| updated_at          | timestamptz | UpdatedTimestamp  |                              |
| external_updated_at | timestamptz | UpdatedTimestamp  |                              |
| seated_at           | timestamp   |                   |                              |
| reservation_id      | uuid        |                   |                              |
| notified_at         | timestamp   |                   |                              |

### `public.restaurant_attributes`

| Column          | Type        | Semantic          | FK Target |
| --------------- | ----------- | ----------------- | --------- |
| restaurant_id   | uuid        |                   |           |
| attribute_type  | text        | Category          |           |
| attribute_value | text        |                   |           |
| created_at      | timestamptz | CreationTimestamp |           |
| updated_at      | timestamptz | UpdatedTimestamp  |           |

### `public.restaurant_events`

| Column        | Type        | Semantic          | FK Target                        |
| ------------- | ----------- | ----------------- | -------------------------------- |
| id            | int4        | PK                |                                  |
| event_id      | uuid        | Category          |                                  |
| restaurant_id | uuid        | FK                | public.restaurants.restaurant_id |
| event_type    | text        | Category          |                                  |
| created_at    | timestamptz | CreationTimestamp |                                  |
| updated_at    | timestamptz | UpdatedTimestamp  |                                  |

### `public.restaurant_groups`

| Column              | Type        | Semantic          | FK Target |
| ------------------- | ----------- | ----------------- | --------- |
| id                  | int4        | PK                |           |
| restaurant_group_id | uuid        |                   |           |
| name                | text        | Name              |           |
| created_at          | timestamptz | CreationTimestamp |           |
| updated_at          | timestamptz | UpdatedTimestamp  |           |

### `public.restaurant_list_entries`

| Column        | Type        | Semantic          | FK Target                        |
| ------------- | ----------- | ----------------- | -------------------------------- |
| id            | int4        | PK                |                                  |
| list_id       | uuid        | FK                | public.restaurant_lists.list_id  |
| restaurant_id | uuid        | FK                | public.restaurants.restaurant_id |
| user_id       | uuid        | FK                | public.users.user_id             |
| created_at    | timestamptz | CreationTimestamp |                                  |
| updated_at    | timestamptz | UpdatedTimestamp  |                                  |

### `public.restaurant_lists`

| Column      | Type        | Semantic          | FK Target            |
| ----------- | ----------- | ----------------- | -------------------- |
| id          | int4        | PK                |                      |
| list_id     | uuid        | Category          |                      |
| user_id     | uuid        | FK                | public.users.user_id |
| list_type   | text        | Category          |                      |
| custom_name | text        |                   |                      |
| created_at  | timestamptz | CreationTimestamp |                      |
| updated_at  | timestamptz | UpdatedTimestamp  |                      |

### `public.restaurant_master_keys`

| Column         | Type        | Semantic          | FK Target                        |
| -------------- | ----------- | ----------------- | -------------------------------- |
| id             | int4        | PK                |                                  |
| restaurant_id  | uuid        | FK                | public.restaurants.restaurant_id |
| master_key_hex | text        |                   |                                  |
| created_at     | timestamptz | CreationTimestamp |                                  |
| updated_at     | timestamptz | UpdatedTimestamp  |                                  |

### `public.restaurant_recommendations`

| Column                       | Type        | Semantic          | FK Target                        |
| ---------------------------- | ----------- | ----------------- | -------------------------------- |
| id                           | int4        | PK                |                                  |
| restaurant_recommendation_id | uuid        | Category          |                                  |
| user_id                      | uuid        | FK                | public.users.user_id             |
| location_id                  | uuid        | FK                | public.locations.location_id     |
| restaurant_id                | uuid        | FK                | public.restaurants.restaurant_id |
| category                     | text        | Category          |                                  |
| created_at                   | timestamptz | CreationTimestamp |                                  |
| updated_at                   | timestamptz | UpdatedTimestamp  |                                  |

### `public.restaurant_user_integrations`

| Column                  | Type        | Semantic | FK Target                                  |
| ----------------------- | ----------- | -------- | ------------------------------------------ |
| id                      | int4        | PK       |                                            |
| restaurant_user_id      | uuid        | FK       | public.restaurant_users.restaurant_user_id |
| provider                | text        |          |                                            |
| access_token            | text        |          |                                            |
| access_token_updated_at | timestamptz |          |                                            |
| created_at              | timestamptz |          |                                            |
| metadata                | text        |          |                                            |

### `public.restaurant_users`

| Column              | Type        | Semantic          | FK Target            |
| ------------------- | ----------- | ----------------- | -------------------- |
| id                  | int4        | PK                |                      |
| restaurant_user_id  | uuid        |                   |                      |
| user_id             | uuid        | FK                | public.users.user_id |
| email               | text        | Email             |                      |
| chat_identity       | text        |                   |                      |
| created_at          | timestamptz | CreationTimestamp |                      |
| updated_at          | timestamptz | UpdatedTimestamp  |                      |
| show_accounting_tab | bool        |                   |                      |

### `public.restaurant_users_locations`

| Column                      | Type        | Semantic          | FK Target                                  |
| --------------------------- | ----------- | ----------------- | ------------------------------------------ |
| id                          | int4        | PK                |                                            |
| restaurant_user_id          | uuid        | FK                | public.restaurant_users.restaurant_user_id |
| location_id                 | uuid        | FK                | public.locations.location_id               |
| created_at                  | timestamptz | CreationTimestamp |                                            |
| updated_at                  | timestamptz | UpdatedTimestamp  |                                            |
| receives_payout_email       | bool        |                   |                                            |
| restaurant_user_location_id | uuid        |                   |                                            |

### `public.restaurants`

| Column                 | Type        | Semantic          | FK Target                                    |
| ---------------------- | ----------- | ----------------- | -------------------------------------------- |
| id                     | int4        | PK                |                                              |
| restaurant_id          | uuid        |                   |                                              |
| name                   | text        | Name              |                                              |
| created_at             | timestamptz | CreationTimestamp |                                              |
| updated_at             | timestamptz | UpdatedTimestamp  |                                              |
| restaurant_group_id    | uuid        | FK                | public.restaurant_groups.restaurant_group_id |
| image                  | text        | URL               |                                              |
| reporting_enabled      | bool        |                   |                                              |
| cuisine                | text        | SerializedJSON    |                                              |
| reward_mode            | text        | Category          |                                              |
| cohort                 | text        | Category          |                                              |
| has_messaging_enabled  | bool        |                   |                                              |
| website_url            | text        | URL               |                                              |
| price                  | text        |                   |                                              |
| score                  | int4        | Score             |                                              |
| instagram_url          | text        | URL               |                                              |
| tiktok_url             | text        | URL               |                                              |
| recommended_items      | varchar     |                   |                                              |
| image_preview          | text        |                   |                                              |
| image_web              | text        |                   |                                              |
| image_full             | text        |                   |                                              |
| image_background_color | text        |                   |                                              |

### `public.restaurants_cuisines`

| Column        | Type        | Semantic          | FK Target                        |
| ------------- | ----------- | ----------------- | -------------------------------- |
| id            | int4        | PK                |                                  |
| cuisine_id    | uuid        | FK                | public.cuisines.cuisine_id       |
| restaurant_id | uuid        | FK                | public.restaurants.restaurant_id |
| created_at    | timestamptz | CreationTimestamp |                                  |
| updated_at    | timestamptz | UpdatedTimestamp  |                                  |

### `public.revinfo`

| Column   | Type | Semantic | FK Target |
| -------- | ---- | -------- | --------- |
| rev      | int4 | PK       |           |
| revtstmp | int8 |          |           |

### `public.reward_listings`

| Column             | Type        | Semantic          | FK Target                          |
| ------------------ | ----------- | ----------------- | ---------------------------------- |
| id                 | int4        | PK                |                                    |
| reward_listing_id  | uuid        |                   |                                    |
| reward_rule_id     | uuid        | FK                | public.reward_rules.reward_rule_id |
| restaurant_id      | uuid        | FK                | public.restaurants.restaurant_id   |
| price_fly          | numeric     |                   |                                    |
| quantity           | int4        | Quantity          |                                    |
| quantity_remaining | int4        | Quantity          |                                    |
| active             | bool        |                   |                                    |
| created_at         | timestamptz | CreationTimestamp |                                    |
| updated_at         | timestamptz | UpdatedTimestamp  |                                    |

### `public.reward_rules`

| Column                    | Type        | Semantic          | FK Target                                  |
| ------------------------- | ----------- | ----------------- | ------------------------------------------ |
| id                        | int4        | PK                |                                            |
| reward_rule_id            | uuid        |                   |                                            |
| restaurant_id             | uuid        |                   |                                            |
| check_in_threshold        | int4        |                   |                                            |
| emoji                     | text        |                   |                                            |
| label                     | text        |                   |                                            |
| description               | text        | Description       |                                            |
| created_at                | timestamptz | CreationTimestamp |                                            |
| updated_at                | timestamptz | UpdatedTimestamp  |                                            |
| internal_label            | text        |                   |                                            |
| internal_description      | text        | Description       |                                            |
| target_membership_tier_id | uuid        | FK                | public.membership_tiers.membership_tier_id |
| active                    | bool        |                   |                                            |
| duration                  | int4        | Duration          |                                            |
| metadata                  | text        | SerializedJSON    |                                            |
| membership_tier_id        | uuid        | FK                | public.membership_tiers.membership_tier_id |
| collaboration_id          | uuid        | FK                | public.collaborations.collaboration_id     |
| fly_reward                | numeric     |                   |                                            |
| is_upcoming               | bool        |                   |                                            |
| target_reward_rule_id     | uuid        | FK                | public.reward_rules.reward_rule_id         |
| image                     | text        | Category          |                                            |
| is_visible_consumer       | bool        |                   |                                            |
| is_visible_restaurant     | bool        |                   |                                            |
| auto_redeemed             | bool        |                   |                                            |
| fly_reward_bips           | int4        |                   |                                            |

### `public.rewards`

| Column         | Type        | Semantic          | FK Target                          |
| -------------- | ----------- | ----------------- | ---------------------------------- |
| id             | int4        | PK                |                                    |
| origin_type    | text        | Category          |                                    |
| origin_id      | uuid        |                   |                                    |
| reward_id      | uuid        |                   |                                    |
| reward_rule_id | uuid        | FK                | public.reward_rules.reward_rule_id |
| user_id        | uuid        | FK                | public.users.user_id               |
| created_at     | timestamptz | CreationTimestamp |                                    |
| updated_at     | timestamptz | UpdatedTimestamp  |                                    |
| expires_at     | timestamptz |                   |                                    |
| membership_id  | uuid        |                   |                                    |
| state          | text        | Category          |                                    |
| check_in_id    | uuid        | FK                | public.check_ins.check_in_id       |

### `public.scheduled_gift_emails`

| Column                 | Type        | Semantic          | FK Target            |
| ---------------------- | ----------- | ----------------- | -------------------- |
| id                     | int4        | PK                |                      |
| payment_id             | uuid        |                   |                      |
| account_transaction_id | uuid        | Category          |                      |
| sender_user_id         | uuid        | FK                | public.users.user_id |
| recipient_name         | text        | Category          |                      |
| recipient_email        | text        | Email             |                      |
| send_at                | timestamptz |                   |                      |
| status                 | text        | Category          |                      |
| created_at             | timestamptz | CreationTimestamp |                      |
| updated_at             | timestamptz | UpdatedTimestamp  |                      |

### `public.scheduled_worker_runs`

| Column                   | Type        | Semantic          | FK Target |
| ------------------------ | ----------- | ----------------- | --------- |
| id                       | uuid        | PK                |           |
| worker_name              | text        | Category          |           |
| started_at               | timestamptz | CreationTimestamp |           |
| last_completed_at        | timestamptz |                   |           |
| last_processed_id        | int8        | Category          |           |
| state                    | text        | Category          |           |
| run_count                | int8        | Quantity          |           |
| max_run_duration_seconds | numeric     | Duration          |           |

### `public.service_configurations`

| Column       | Type      | Semantic          | FK Target |
| ------------ | --------- | ----------------- | --------- |
| id           | int4      | PK                |           |
| key          | text      | PK                |           |
| value        | text      | Category          |           |
| created_at   | timestamp | CreationTimestamp |           |
| updated_at   | timestamp | UpdatedTimestamp  |           |
| service_name | text      | Category          |           |

### `public.statuses`

| Column                   | Type        | Semantic          | FK Target |
| ------------------------ | ----------- | ----------------- | --------- |
| id                       | int4        | PK                |           |
| status_id                | uuid        | Category          |           |
| name                     | text        | Name              |           |
| level                    | int4        | Category          |           |
| description              | text        | Description       |           |
| fly_multiplier           | int4        | Category          |           |
| fly_deposit_threshold    | numeric     |                   |           |
| spend_threshold          | int4        | Category          |           |
| check_in_threshold       | int4        | Category          |           |
| year_start               | int4        | Category          |           |
| year_end                 | int4        |                   |           |
| created_at               | timestamptz | CreationTimestamp |           |
| updated_at               | timestamptz | UpdatedTimestamp  |           |
| max_reservation_requests | int4        | Category          |           |
| track                    | text        | Category          |           |
| benefits                 | jsonb       | SerializedJSON    |           |
| title                    | text        | Title             |           |
| byline                   | text        |                   |           |
| disclaimers              | jsonb       | SerializedJSON    |           |
| nft_status_id            | int4        | Category          |           |
| image_url                | text        | URL               |           |

### `public.subscription_terms`

| Column               | Type        | Semantic          | FK Target                  |
| -------------------- | ----------- | ----------------- | -------------------------- |
| id                   | int4        | PK                |                            |
| subscription_term_id | uuid        | Subscription      |                            |
| pass_id              | uuid        | FK                | public.passes.pass_id      |
| payment_id           | uuid        | FK                | public.payments.payment_id |
| starts_at            | timestamptz | CreationTimestamp |                            |
| renews_at            | timestamptz |                   |                            |
| created_at           | timestamptz | CreationTimestamp |                            |
| updated_at           | timestamptz | UpdatedTimestamp  |                            |
| status               | text        | Category          |                            |

### `public.sun_data_entries`

| Column     | Type        | Semantic          | FK Target |
| ---------- | ----------- | ----------------- | --------- |
| id         | int4        | PK                |           |
| entry_id   | uuid        |                   |           |
| user_id    | uuid        |                   |           |
| cmac       | text        |                   |           |
| picc_data  | text        |                   |           |
| read_ctr   | int4        |                   |           |
| created_at | timestamptz | CreationTimestamp |           |
| updated_at | timestamptz | UpdatedTimestamp  |           |

### `public.temp_darsh_loctions`

| Column            | Type | Semantic       | FK Target |
| ----------------- | ---- | -------------- | --------- |
| location_id       | text |                |           |
| reservation_url   | text | URL            |           |
| restaurant_id     | text |                |           |
| instagram_url     | text | URL            |           |
| what_to_know      | text | SerializedJSON |           |
| recommended_items | text | SerializedJSON |           |
| id_location       | text |                |           |
| id_restaurant     | text |                |           |

### `public.user_cuisine_category_scores`

| Column              | Type        | Semantic          | FK Target                                     |
| ------------------- | ----------- | ----------------- | --------------------------------------------- |
| id                  | int4        | PK                |                                               |
| cuisine_category_id | uuid        | FK                | public.cuisine_categories.cuisine_category_id |
| user_id             | uuid        | FK                | public.users.user_id                          |
| check_in_count      | int4        | Quantity          |                                               |
| created_at          | timestamptz | CreationTimestamp |                                               |
| updated_at          | timestamptz | UpdatedTimestamp  |                                               |

### `public.user_devices`

| Column         | Type        | Semantic          | FK Target            |
| -------------- | ----------- | ----------------- | -------------------- |
| id             | int4        | PK                |                      |
| user_device_id | uuid        |                   |                      |
| user_id        | uuid        | FK                | public.users.user_id |
| platform       | text        | Category          |                      |
| version        | text        | Category          |                      |
| created_at     | timestamptz | CreationTimestamp |                      |
| updated_at     | timestamptz | UpdatedTimestamp  |                      |
| user_agent     | text        |                   |                      |

### `public.user_incentive_activities`

| Column                     | Type        | Semantic          | FK Target                                |
| -------------------------- | ----------- | ----------------- | ---------------------------------------- |
| user_incentive_activity_id | uuid        | Category          |                                          |
| user_incentive_id          | uuid        | FK                | public.user_incentives.user_incentive_id |
| activity_type              | text        | Category          |                                          |
| activity_id                | uuid        | Category          |                                          |
| spend_amount               | numeric     |                   |                                          |
| created_at                 | timestamptz | CreationTimestamp |                                          |
| updated_at                 | timestamptz | UpdatedTimestamp  |                                          |

### `public.user_incentives`

| Column            | Type        | Semantic          | FK Target                      |
| ----------------- | ----------- | ----------------- | ------------------------------ |
| id                | int4        | PK                |                                |
| user_incentive_id | uuid        |                   |                                |
| incentive_id      | uuid        | FK                | public.incentives.incentive_id |
| user_id           | uuid        | FK                | public.users.user_id           |
| status            | text        | Category          |                                |
| expires_at        | timestamp   |                   |                                |
| completed_at      | timestamp   |                   |                                |
| created_at        | timestamp   | CreationTimestamp |                                |
| updated_at        | timestamp   | UpdatedTimestamp  |                                |
| current_progress  | numeric     |                   |                                |
| enrolled_at       | timestamptz |                   |                                |

### `public.user_media_views`

| Column             | Type        | Semantic          | FK Target             |
| ------------------ | ----------- | ----------------- | --------------------- |
| id                 | int4        | PK                |                       |
| user_media_view_id | uuid        | PK                |                       |
| user_id            | uuid        | FK                | public.users.user_id  |
| media_id           | uuid        | FK                | public.media.media_id |
| created_at         | timestamptz | CreationTimestamp |                       |
| updated_at         | timestamptz | UpdatedTimestamp  |                       |

### `public.user_notifications`

| Column               | Type        | Semantic          | FK Target                    |
| -------------------- | ----------- | ----------------- | ---------------------------- |
| id                   | int4        | PK                |                              |
| user_notification_id | uuid        |                   |                              |
| user_id              | uuid        | FK                | public.users.user_id         |
| location_id          | uuid        | FK                | public.locations.location_id |
| entity_type          | text        | Category          |                              |
| entity_id            | uuid        |                   |                              |
| message_body         | text        |                   |                              |
| read_at              | timestamptz |                   |                              |
| created_at           | timestamptz | CreationTimestamp |                              |
| updated_at           | timestamptz | UpdatedTimestamp  |                              |

### `public.user_preferences`

| Column                 | Type        | Semantic          | FK Target            |
| ---------------------- | ----------- | ----------------- | -------------------- |
| id                     | int4        | PK                |                      |
| user_id                | uuid        | FK                | public.users.user_id |
| data_sharing_enabled   | bool        |                   |                      |
| created_at             | timestamptz | CreationTimestamp |                      |
| updated_at             | timestamptz | UpdatedTimestamp  |                      |
| default_tip_percentage | int4        | Category          |                      |
| learn_blackbird        | bool        |                   |                      |
| learn_fly              | bool        |                   |                      |

### `public.user_price_scores`

| Column         | Type        | Semantic          | FK Target            |
| -------------- | ----------- | ----------------- | -------------------- |
| id             | int4        | PK                |                      |
| user_id        | uuid        | FK                | public.users.user_id |
| price          | text        | Category          |                      |
| check_in_count | int4        | Quantity          |                      |
| created_at     | timestamptz | CreationTimestamp |                      |
| updated_at     | timestamptz | UpdatedTimestamp  |                      |

### `public.user_status_overrides`

| Column      | Type        | Semantic          | FK Target                 |
| ----------- | ----------- | ----------------- | ------------------------- |
| id          | int4        | PK                |                           |
| user_id     | uuid        | FK                | public.users.user_id      |
| status_id   | uuid        | FK                | public.statuses.status_id |
| starts_at   | timestamptz | CreationTimestamp |                           |
| ends_at     | timestamptz |                   |                           |
| created_at  | timestamptz | CreationTimestamp |                           |
| updated_at  | timestamptz | UpdatedTimestamp  |                           |
| origin_id   | uuid        |                   |                           |
| origin_type | text        | Category          |                           |

### `public.user_status_progress`

| Column                  | Type        | Semantic          | FK Target            |
| ----------------------- | ----------- | ----------------- | -------------------- |
| id                      | int4        | PK                |                      |
| user_id                 | uuid        | FK                | public.users.user_id |
| year                    | int4        | Category          |                      |
| check_ins               | int4        | Category          |                      |
| spend                   | int4        | Category          |                      |
| fly_deposit             | numeric     |                   |                      |
| created_at              | timestamptz | CreationTimestamp |                      |
| updated_at              | timestamptz | UpdatedTimestamp  |                      |
| user_status_progress_id | uuid        | Category          |                      |

### `public.user_statuses`

| Column         | Type        | Semantic          | FK Target                 |
| -------------- | ----------- | ----------------- | ------------------------- |
| id             | int4        | PK                |                           |
| user_status_id | uuid        | Category          |                           |
| user_id        | uuid        | FK                | public.users.user_id      |
| status_id      | uuid        | FK                | public.statuses.status_id |
| state          | text        | Category          |                           |
| started_at     | timestamptz | CreationTimestamp |                           |
| ended_at       | timestamptz |                   |                           |
| created_at     | timestamptz | CreationTimestamp |                           |
| updated_at     | timestamptz | UpdatedTimestamp  |                           |

### `public.user_statuses_aud`

| Column  | Type | Semantic | FK Target          |
| ------- | ---- | -------- | ------------------ |
| id      | int4 | PK       |                    |
| rev     | int4 | FK       | public.revinfo.rev |
| revtype | int2 | Category |                    |
| state   | text | Category |                    |

### `public.user_tags`

| Column      | Type          | Semantic          | FK Target            |
| ----------- | ------------- | ----------------- | -------------------- |
| id          | int4          | PK                |                      |
| user_tag_id | uuid          | Category          |                      |
| user_id     | uuid          | FK                | public.users.user_id |
| type        | user_tag_type | Category          |                      |
| metadata    | jsonb         | SerializedJSON    |                      |
| created_at  | timestamptz   | CreationTimestamp |                      |
| updated_at  | timestamptz   | UpdatedTimestamp  |                      |

### `public.user_terms`

| Column     | Type        | Semantic | FK Target            |
| ---------- | ----------- | -------- | -------------------- |
| id         | int4        | PK       |                      |
| user_id    | uuid        | FK       | public.users.user_id |
| version    | date        |          |                      |
| platform   | text        |          |                      |
| app_name   | text        |          |                      |
| created_at | timestamptz |          |                      |
| updated_at | timestamptz |          |                      |

### `public.user_wallet_permits`

| Column           | Type        | Semantic          | FK Target |
| ---------------- | ----------- | ----------------- | --------- |
| id               | int4        | PK                |           |
| wallet_permit_id | uuid        | Category          |           |
| signature_id     | uuid        | Category          |           |
| transaction_id   | uuid        |                   |           |
| status           | text        | Category          |           |
| user_id          | uuid        | Category          |           |
| user_wallet_id   | uuid        | Category          |           |
| currency         | text        | Category          |           |
| created_at       | timestamptz | CreationTimestamp |           |
| updated_at       | timestamptz | UpdatedTimestamp  |           |

### `public.user_wallets`

| Column         | Type        | Semantic          | FK Target            |
| -------------- | ----------- | ----------------- | -------------------- |
| id             | int4        | PK                |                      |
| user_wallet_id | uuid        |                   |                      |
| user_id        | uuid        | FK                | public.users.user_id |
| wallet_type    | text        | Category          |                      |
| address        | text        |                   |                      |
| provider_index | int4        | Category          |                      |
| created_at     | timestamptz | CreationTimestamp |                      |
| updated_at     | timestamptz | UpdatedTimestamp  |                      |

### `public.users`

| Column             | Type        | Semantic          | FK Target |
| ------------------ | ----------- | ----------------- | --------- |
| id                 | int4        | PK                |           |
| user_id            | uuid        |                   |           |
| first_name         | text        | Name              |           |
| last_name          | text        | Name              |           |
| phone_number       | text        |                   |           |
| country_code       | text        | Country           |           |
| created_at         | timestamptz | CreationTimestamp |           |
| updated_at         | timestamptz | UpdatedTimestamp  |           |
| email              | text        |                   |           |
| zipcode            | text        | ZipCode           |           |
| birthdate          | date        | Birthdate         |           |
| fly_multiplier     | int4        | Category          |           |
| avatar             | text        |                   |           |
| active             | bool        |                   |           |
| chat_identity      | text        |                   |           |
| discord            | text        |                   |           |
| wallet_provider_id | text        |                   |           |
| account_status     | text        | State             |           |
| internal           | bool        |                   |           |

### `public.users_aud`

| Column         | Type        | Semantic          | FK Target          |
| -------------- | ----------- | ----------------- | ------------------ |
| id             | int4        | PK                |                    |
| rev            | int4        | FK                | public.revinfo.rev |
| revtype        | int2        | Category          |                    |
| phone_number   | text        |                   |                    |
| fly_multiplier | int4        | Category          |                    |
| active         | bool        |                   |                    |
| account_status | text        | State             |                    |
| created_at     | timestamptz | CreationTimestamp |                    |

### `public.users_neighborhoods_scores`

| Column          | Type        | Semantic          | FK Target                            |
| --------------- | ----------- | ----------------- | ------------------------------------ |
| id              | int4        | PK                |                                      |
| user_id         | uuid        | FK                | public.users.user_id                 |
| neighborhood_id | uuid        | FK                | public.neighborhoods.neighborhood_id |
| check_in_count  | int4        | Quantity          |                                      |
| created_at      | timestamptz | CreationTimestamp |                                      |
| updated_at      | timestamptz | UpdatedTimestamp  |                                      |

### `public.waitlist_entries`

| Column      | Type        | Semantic          | FK Target            |
| ----------- | ----------- | ----------------- | -------------------- |
| id          | int4        | PK                |                      |
| email       | text        | Email             |                      |
| first_name  | text        | Name              |                      |
| last_name   | text        | Name              |                      |
| target_id   | uuid        | Category          |                      |
| target_type | text        | Category          |                      |
| created_at  | timestamptz | CreationTimestamp |                      |
| updated_at  | timestamptz | UpdatedTimestamp  |                      |
| user_id     | uuid        | FK                | public.users.user_id |

### `public.wallet_signatures`

| Column                     | Type        | Semantic          | FK Target |
| -------------------------- | ----------- | ----------------- | --------- |
| id                         | int4        | PK                |           |
| signature_id               | uuid        | Category          |           |
| created_at                 | timestamptz | CreationTimestamp |           |
| updated_at                 | timestamptz | UpdatedTimestamp  |           |
| is_active                  | bool        |                   |           |
| entity_id                  | uuid        | Category          |           |
| wallet_id                  | uuid        | Category          |           |
| from_address               | text        | Category          |           |
| to_address                 | text        | Category          |           |
| value_amount               | numeric     |                   |           |
| valid_after                | text        | Category          |           |
| valid_before               | text        | Category          |           |
| nonce                      | text        | Category          |           |
| signature                  | text        | Category          |           |
| chain_id                   | numeric     |                   |           |
| contract_name              | text        | Category          |           |
| verifying_contract_address | text        | Category          |           |
| owner                      | text        | Owner             |           |
| spender                    | text        |                   |           |
| deadline                   | text        |                   |           |
| function_name              | text        | Category          |           |

### `public.webhook_events`

| Column                                                                                       | Type        | Semantic          | FK Target |
| -------------------------------------------------------------------------------------------- | ----------- | ----------------- | --------- |
| id                                                                                           | int4        | PK                |           |
| payload → created_at                                                                         | timestamp   | CreationTimestamp |           |
| payload → created_on                                                                         | timestamp   | CreationTimestamp |           |
| payload → data → balances → available_to_capture                                             | decimal     |                   |           |
| payload → data → balances → total_authorized                                                 | decimal     | Author            |           |
| payload → data → currency                                                                    | text        |                   |           |
| payload → data → customer → email                                                            | text        |                   |           |
| payload → data → eci                                                                         | text        |                   |           |
| payload → data → event_links → payment_actions                                               | text        |                   |           |
| payload → data → object → order_created → created_at                                         | timestamp   | CreationTimestamp |           |
| payload → data → object → order_created → location_id                                        | text        |                   |           |
| payload → data → object → order_created → order_id                                           | text        |                   |           |
| payload → data → object → order_created → state                                              | text        |                   |           |
| payload → data → object → order_updated → created_at                                         | timestamp   | CreationTimestamp |           |
| payload → data → object → order_updated → order_id                                           | text        |                   |           |
| payload → data → object → order_updated → state                                              | text        |                   |           |
| payload → data → object → order_updated → updated_at                                         | timestamp   | UpdatedTimestamp  |           |
| payload → data → object → order_updated → version                                            | decimal     |                   |           |
| payload → data → object → payment → amount_money → currency                                  | text        |                   |           |
| payload → data → object → payment → app_fee_money → amount                                   | decimal     |                   |           |
| payload → data → object → payment → app_fee_money → currency                                 | text        |                   |           |
| payload → data → object → payment → application_details → application_id                     | text        |                   |           |
| payload → data → object → payment → approved_money → currency                                | text        |                   |           |
| payload → data → object → payment → billing_address → address_line_1                         | text        |                   |           |
| payload → data → object → payment → billing_address → country                                | text        |                   |           |
| payload → data → object → payment → billing_address → first_name                             | text        |                   |           |
| payload → data → object → payment → billing_address → locality                               | text        |                   |           |
| payload → data → object → payment → billing_address → postal_code                            | text        |                   |           |
| payload → data → object → payment → card_details → application_cryptogram                    | text        |                   |           |
| payload → data → object → payment → card_details → application_identifier                    | text        |                   |           |
| payload → data → object → payment → card_details → auth_result_code                          | text        |                   |           |
| payload → data → object → payment → card_details → avs_status                                | text        |                   |           |
| payload → data → object → payment → card_details → card → card_brand                         | text        |                   |           |
| payload → data → object → payment → card_details → card → exp_year                           | decimal     |                   |           |
| payload → data → object → payment → card_details → card → fingerprint                        | text        |                   |           |
| payload → data → object → payment → card_details → card → last_4                             | text        |                   |           |
| payload → data → object → payment → card_details → card → payment_account_reference          | text        |                   |           |
| payload → data → object → payment → card_details → card_payment_timeline → authorized_at     | timestamp   |                   |           |
| payload → data → object → payment → card_details → card_payment_timeline → captured_at       | timestamp   |                   |           |
| payload → data → object → payment → card_details → cvv_status                                | text        |                   |           |
| payload → data → object → payment → card_details → device_details → device_installation_id   | text        |                   |           |
| payload → data → object → payment → card_details → device_details → device_name              | text        |                   |           |
| payload → data → object → payment → card_details → emv_details → authorization_response_code | text        | Author            |           |
| payload → data → object → payment → card_details → statement_description                     | text        | Description       |           |
| payload → data → object → payment → card_details → verification_method                       | text        |                   |           |
| payload → data → object → payment → card_details → verification_results                      | text        |                   |           |
| payload → data → object → payment → cash_details → buyer_supplied_money → amount             | decimal     |                   |           |
| payload → data → object → payment → customer_id                                              | text        |                   |           |
| payload → data → object → payment → delay_duration                                           | text        |                   |           |
| payload → data → object → payment → device_details → device_id                               | text        |                   |           |
| payload → data → object → payment → external_details → source                                | text        | Source            |           |
| payload → data → object → payment → external_details → type                                  | text        |                   |           |
| payload → data → object → payment → location_id                                              | text        |                   |           |
| payload → data → object → payment → order_id                                                 | text        |                   |           |
| payload → data → object → payment → receipt_url                                              | text        | URL               |           |
| payload → data → object → payment → risk_evaluation → created_at                             | timestamp   | CreationTimestamp |           |
| payload → data → object → payment → shipping_address → first_name                            | text        |                   |           |
| payload → data → object → payment → source_type                                              | text        | Category          |           |
| payload → data → object → payment → tip_money → amount                                       | decimal     |                   |           |
| payload → data → object → payment → total_money → amount                                     | decimal     |                   |           |
| payload → data → pan_type_processed                                                          | text        |                   |           |
| payload → data → payment_account_reference                                                   | text        |                   |           |
| payload → data → processed_on                                                                | text        | Category          |           |
| payload → data → processing → acquirer_reference_number                                      | text        |                   |           |
| payload → data → processing → acquirer_transaction_id                                        | text        |                   |           |
| payload → data → processing → aft                                                            | text        |                   |           |
| payload → data → processing → card_acceptor_id                                               | text        |                   |           |
| payload → data → processing_channel_id                                                       | text        | Source            |           |
| payload → data → processing → partner_response_code                                          | text        |                   |           |
| payload → data → processing → retrieval_reference_number                                     | text        |                   |           |
| payload → data → processing → scheme                                                         | text        |                   |           |
| payload → data → processing → scheme_merchant_id                                             | text        |                   |           |
| payload → data → reference                                                                   | text        |                   |           |
| payload → data → response_code                                                               | text        |                   |           |
| payload → data → response_summary                                                            | text        |                   |           |
| payload → data → scheme_id                                                                   | text        |                   |           |
| payload → data → source → account_holder → account_name_inquiry                              | text        | Source            |           |
| payload → data → source → account_holder → account_name_inquiry_details → first_name         | text        | Source            |           |
| payload → data → source → account_holder → last_name                                         | text        | Source            |           |
| payload → data → source → account_holder → type                                              | text        | Source            |           |
| payload → data → source → billing_address → country                                          | text        | Source            |           |
| payload → data → source → billing_address → state                                            | text        | Source            |           |
| payload → data → source → billing_address → town_city                                        | text        | Source            |           |
| payload → data → source → billing_address → zip                                              | text        | Source            |           |
| payload → data → source → card_wallet_type                                                   | text        | Category          |           |
| payload → data → source → cvv_check                                                          | text        | Source            |           |
| payload → data → source → fingerprint                                                        | text        | Source            |           |
| payload → data → source → issuer                                                             | text        | Source            |           |
| payload → data → source → last_4                                                             | text        | Source            |           |
| payload → data → source → local_schemes                                                      | text        |                   |           |
| payload → data → source → product_id                                                         | text        | Source            |           |
| payload → data → source → product_type                                                       | text        | Category          |           |
| payload → data → source → type                                                               | text        | Source            |           |
| payload → data → type                                                                        | text        |                   |           |
| payload → event_id                                                                           | text        |                   |           |
| payload → id                                                                                 | text        |                   |           |
| payload → \_links → payment → href                                                           | text        |                   |           |
| payload → \_links → refund → href                                                            | text        |                   |           |
| payload → merchant_id                                                                        | text        |                   |           |
| payload → type                                                                               | text        |                   |           |
| payload → version                                                                            | text        |                   |           |
| webhook_event_id                                                                             | uuid        |                   |           |
| route                                                                                        | text        | Category          |           |
| payload                                                                                      | jsonb       | SerializedJSON    |           |
| created_at                                                                                   | timestamptz | CreationTimestamp |           |
| updated_at                                                                                   | timestamptz | UpdatedTimestamp  |           |

## Schema: square

### Tables:

- orders
- payments
- tokens
- transactions

### `square.orders`

| Column                                                  | Type        | Semantic          | FK Target                    |
| ------------------------------------------------------- | ----------- | ----------------- | ---------------------------- |
| id                                                      | int4        | PK                |                              |
| payload → closed_at                                     | timestamp   |                   |                              |
| payload → created_at                                    | timestamp   | CreationTimestamp |                              |
| payload → customer_id                                   | text        |                   |                              |
| payload → discounts                                     | text        |                   |                              |
| payload → fulfillments                                  | text        |                   |                              |
| payload → id                                            | text        |                   |                              |
| payload → line_items                                    | text        |                   |                              |
| payload → location_id                                   | text        | Category          |                              |
| payload → net_amount_due_money → amount                 | decimal     |                   |                              |
| payload → net_amount_due_money → currency               | text        | Category          |                              |
| payload → net_amounts → card_surcharge_money → amount   | decimal     |                   |                              |
| payload → net_amounts → card_surcharge_money → currency | text        |                   |                              |
| payload → net_amounts → discount_money → amount         | decimal     | Discount          |                              |
| payload → net_amounts → discount_money → currency       | text        | Category          |                              |
| payload → net_amounts → service_charge_money → amount   | decimal     | Category          |                              |
| payload → net_amounts → service_charge_money → currency | text        | Category          |                              |
| payload → net_amounts → tax_money → amount              | decimal     |                   |                              |
| payload → net_amounts → tax_money → currency            | text        | Category          |                              |
| payload → net_amounts → tip_money → amount              | decimal     |                   |                              |
| payload → net_amounts → tip_money → currency            | text        | Category          |                              |
| payload → net_amounts → total_money → amount            | decimal     |                   |                              |
| payload → net_amounts → total_money → currency          | text        | Category          |                              |
| payload → pricing_options → auto_apply_discounts        | boolean     |                   |                              |
| payload → pricing_options → auto_apply_taxes            | boolean     |                   |                              |
| payload → reference_id                                  | text        |                   |                              |
| payload → rewards                                       | text        |                   |                              |
| payload → source → name                                 | text        | Source            |                              |
| payload → state                                         | text        | Category          |                              |
| payload → taxes                                         | text        |                   |                              |
| payload → tenders                                       | text        |                   |                              |
| payload → ticket_name                                   | text        |                   |                              |
| payload → total_card_surcharge_money → amount           | decimal     |                   |                              |
| payload → total_card_surcharge_money → currency         | text        |                   |                              |
| payload → total_discount_money → amount                 | decimal     | Discount          |                              |
| payload → total_discount_money → currency               | text        | Category          |                              |
| payload → total_money → amount                          | decimal     |                   |                              |
| payload → total_money → currency                        | text        | Category          |                              |
| payload → total_service_charge_money → amount           | decimal     | Category          |                              |
| payload → total_service_charge_money → currency         | text        | Category          |                              |
| payload → total_tax_money → amount                      | decimal     |                   |                              |
| payload → total_tax_money → currency                    | text        | Category          |                              |
| payload → total_tip_money → amount                      | decimal     |                   |                              |
| payload → total_tip_money → currency                    | text        | Category          |                              |
| payload → updated_at                                    | timestamp   | UpdatedTimestamp  |                              |
| payload → version                                       | decimal     |                   |                              |
| order_id                                                | uuid        |                   |                              |
| location_id                                             | uuid        | FK                | public.locations.location_id |
| external_id                                             | text        |                   |                              |
| payload                                                 | jsonb       | SerializedJSON    |                              |
| created_at                                              | timestamptz | CreationTimestamp |                              |
| updated_at                                              | timestamptz | UpdatedTimestamp  |                              |

### `square.payments`

| Column      | Type        | Semantic          | FK Target                    |
| ----------- | ----------- | ----------------- | ---------------------------- |
| id          | int4        | PK                |                              |
| payment_id  | uuid        |                   |                              |
| location_id | uuid        | FK                | public.locations.location_id |
| external_id | text        |                   |                              |
| payload     | jsonb       | SerializedJSON    |                              |
| created_at  | timestamptz | CreationTimestamp |                              |
| updated_at  | timestamptz | UpdatedTimestamp  |                              |

### `square.tokens`

| Column        | Type        | Semantic          | FK Target |
| ------------- | ----------- | ----------------- | --------- |
| id            | int4        | PK                |           |
| token_id      | uuid        |                   |           |
| access_token  | text        |                   |           |
| refresh_token | text        | Category          |           |
| created_at    | timestamptz | CreationTimestamp |           |
| updated_at    | timestamptz | UpdatedTimestamp  |           |

### `square.transactions`

| Column                  | Type        | Semantic          | FK Target                    |
| ----------------------- | ----------- | ----------------- | ---------------------------- |
| id                      | int4        | PK                |                              |
| transaction_id          | uuid        |                   |                              |
| location_id             | uuid        | FK                | public.locations.location_id |
| external_transaction_id | text        |                   |                              |
| date                    | date        |                   |                              |
| time                    | time        |                   |                              |
| time_zone               | text        | Category          |                              |
| gross_sales             | int8        |                   |                              |
| discounts               | int8        | Discount          |                              |
| service_charges         | int8        | Category          |                              |
| net_sales               | int8        |                   |                              |
| gift_card_sales         | int8        | Category          |                              |
| tax                     | int8        |                   |                              |
| tip                     | int8        |                   |                              |
| partial_refunds         | int8        | Category          |                              |
| total_collected         | int8        |                   |                              |
| source                  | text        | Source            |                              |
| card                    | int8        |                   |                              |
| card_entry_method       | text        | Category          |                              |
| square_gift_card        | int8        | Category          |                              |
| other_tender            | int8        | Category          |                              |
| other_tender_type       | text        | Category          |                              |
| fees                    | int8        |                   |                              |
| net_total               | int8        |                   |                              |
| payment_id              | text        |                   |                              |
| card_brand              | text        | Category          |                              |
| pan_suffix              | text        |                   |                              |
| device_name             | text        | Category          |                              |
| staff_name              | text        | Category          |                              |
| staff_id                | text        |                   |                              |
| details                 | text        | URL               |                              |
| description             | text        | Description       |                              |
| event_type              | text        | Category          |                              |
| external_location       | text        | Category          |                              |
| dining_option           | text        |                   |                              |
| customer_id             | text        |                   |                              |
| customer_name           | text        |                   |                              |
| customer_reference_id   | text        |                   |                              |
| device_nickname         | text        |                   |                              |
| third_party_fees        | int8        | Category          |                              |
| deposit_id              | text        |                   |                              |
| deposit_date            | text        |                   |                              |
| deposit_details         | text        |                   |                              |
| fee_percentage          | text        |                   |                              |
| fee_fixed_rate          | text        | Category          |                              |
| refund_reason           | text        | Category          |                              |
| discount_name           | text        | Category          |                              |
| transaction_status      | text        | Category          |                              |
| cash_app                | int8        | Category          |                              |
| order_reference_id      | text        |                   |                              |
| fulfillment_note        | text        |                   |                              |
| free_processing_applied | int8        | Category          |                              |
| in_store_code           | text        |                   |                              |
| created_at              | timestamptz | CreationTimestamp |                              |
| updated_at              | timestamptz | UpdatedTimestamp  |                              |

## Schema: supergood_toast

### Tables:

- checks
- credentials

### `supergood_toast.checks`

| Column                               | Type        | Semantic          | FK Target                    |
| ------------------------------------ | ----------- | ----------------- | ---------------------------- |
| id                                   | int4        | PK                |                              |
| payload → guestFeedback              | text        |                   |                              |
| payload → payments                   | text        |                   |                              |
| payload → pricing → amount           | text        |                   |                              |
| payload → pricing → amountDue        | text        |                   |                              |
| payload → pricing → appliedDiscounts | text        |                   |                              |
| payload → pricing → currency         | text        | Category          |                              |
| payload → pricing → taxAmount        | text        |                   |                              |
| payload → pricing → tipAmount        | text        |                   |                              |
| payload → pricing → tipPercentage    | decimal     |                   |                              |
| payload → pricing → totalAmount      | text        |                   |                              |
| payload → selections                 | text        |                   |                              |
| check_id                             | uuid        |                   |                              |
| location_id                          | uuid        | FK                | public.locations.location_id |
| external_id                          | uuid        |                   |                              |
| external_order_id                    | uuid        |                   |                              |
| payload                              | jsonb       | SerializedJSON    |                              |
| created_at                           | timestamptz | CreationTimestamp |                              |
| updated_at                           | timestamptz | UpdatedTimestamp  |                              |

### `supergood_toast.credentials`

| Column        | Type        | Semantic          | FK Target |
| ------------- | ----------- | ----------------- | --------- |
| id            | int4        | PK                |           |
| credential_id | uuid        | Category          |           |
| username      | text        | Email             |           |
| password      | text        | Category          |           |
| auth_token    | text        | Category          |           |
| created_at    | timestamptz | CreationTimestamp |           |
| updated_at    | timestamptz | UpdatedTimestamp  |           |

## Schema: toast

### Tables:

- export_configs
- order_records

### `toast.export_configs`

| Column           | Type      | Semantic          | FK Target                    |
| ---------------- | --------- | ----------------- | ---------------------------- |
| id               | int4      | PK                |                              |
| export_config_id | uuid      | Category          |                              |
| username         | text      | Category          |                              |
| server_url       | text      | URL               |                              |
| export_id        | int4      | Category          |                              |
| is_active        | bool      |                   |                              |
| location_id      | uuid      | FK                | public.locations.location_id |
| updated_at       | timestamp | UpdatedTimestamp  |                              |
| created_at       | timestamp | CreationTimestamp |                              |

### `toast.order_records`

| Column          | Type        | Semantic          | FK Target                    |
| --------------- | ----------- | ----------------- | ---------------------------- |
| id              | int4        | PK                |                              |
| order_record_id | uuid        |                   |                              |
| payment_id      | text        |                   |                              |
| location_id     | uuid        | FK                | public.locations.location_id |
| order_number    | int4        | Quantity          |                              |
| order_date      | timestamptz |                   |                              |
| tab_name        | text        |                   |                              |
| server          | text        |                   |                              |
| table_name      | text        | Category          |                              |
| dining_area     | text        | Category          |                              |
| service         | text        | Category          |                              |
| dining_option   | text        |                   |                              |
| amount          | numeric     |                   |                              |
| tip             | numeric     |                   |                              |
| gratuity        | numeric     |                   |                              |
| total           | numeric     |                   |                              |
| void_date       | timestamptz |                   |                              |
| other_type      | text        | Category          |                              |
| processed_at    | timestamptz |                   |                              |
| created_at      | timestamptz | CreationTimestamp |                              |
| updated_at      | timestamptz | UpdatedTimestamp  |                              |
| type            | text        | Category          |                              |
| card_type       | text        | Category          |                              |

---

# Foreign Key Relationships

| From                                                       | To                                                   |
| ---------------------------------------------------------- | ---------------------------------------------------- |
| public.account_balances_aud.rev                            | public.revinfo.rev                                   |
| public.account_transactions.blackbird_payment_id           | public.blackbird_payments.blackbird_payment_id       |
| public.activation_events.location_id                       | public.locations.location_id                         |
| public.adjustments.check_share_id                          | public.check_shares.check_share_id                   |
| public.adjustments.payout_id                               | public.payouts.payout_id                             |
| public.banking_person_application_forms.restaurant_user_id | public.restaurant_users.restaurant_user_id           |
| public.billing_addresses.user_id                           | public.users.user_id                                 |
| public.blackbird_payments.card_payment_id                  | public.payments.payment_id                           |
| public.blackbird_payments.promotion_code_id                | public.promotion_codes.promotion_code_id             |
| public.blackbird_payments.user_id                          | public.users.user_id                                 |
| public.cards.billing_address_id                            | public.billing_addresses.billing_address_id          |
| public.cards.user_id                                       | public.users.user_id                                 |
| public.check_ins.membership_id                             | public.memberships.membership_id                     |
| public.check_ins.nfc_chip_id                               | public.nfc_chips.nfc_chip_id                         |
| public.check_ins.restaurant_id                             | public.restaurants.restaurant_id                     |
| public.check_ins.user_id                                   | public.users.user_id                                 |
| public.check_shares.check_id                               | public.checks.check_id                               |
| public.check_shares.check_in_id                            | public.check_ins.check_in_id                         |
| public.check_shares.payment_method_id                      | public.cards.card_id                                 |
| public.check_shares.user_id                                | public.users.user_id                                 |
| public.check_shares_aud.rev                                | public.revinfo.rev                                   |
| public.checks.closing_employee_id                          | public.employees.employee_id                         |
| public.checks.location_id                                  | public.locations.location_id                         |
| public.checks.payment_method_id                            | public.cards.card_id                                 |
| public.checks.payout_id                                    | public.payouts.payout_id                             |
| public.checks_aud.rev                                      | public.revinfo.rev                                   |
| public.chits.user_id                                       | public.users.user_id                                 |
| public.collaboration_perks.collaboration_id                | public.collaborations.collaboration_id               |
| public.collaboration_restaurants.collaboration_id          | public.collaborations.collaboration_id               |
| public.collaboration_restaurants.restaurant_id             | public.restaurants.restaurant_id                     |
| public.collaborations.primary_region_id                    | public.regions.region_id                             |
| public.conversation_messages.conversation_id               | public.conversations.id                              |
| public.conversations.location_id                           | public.locations.location_id                         |
| public.conversations.user_id                               | public.users.user_id                                 |
| public.cuisines.cuisine_category_id                        | public.cuisine_categories.cuisine_category_id        |
| public.curated_recommendations.location_id                 | public.locations.location_id                         |
| public.curated_recommendations.region_id                   | public.regions.region_id                             |
| public.employee_check_actions.check_id                     | public.checks.check_id                               |
| public.employee_check_actions.employee_id                  | public.employees.employee_id                         |
| public.employee_incentive_progresses.employee_id           | public.employees.employee_id                         |
| public.employee_incentive_progresses.employee_incentive_id | public.employee_incentives.employee_incentive_id     |
| public.employee_incentives.location_id                     | public.locations.location_id                         |
| public.employee_pin_tokens.employee_id                     | public.employees.employee_id                         |
| public.employees.location_id                               | public.locations.location_id                         |
| public.employees.user_id                                   | public.users.user_id                                 |
| public.failed_sessions.user_id                             | public.users.user_id                                 |
| public.fly_ledger_entries.account_balance_id               | public.account_balances.account_balance_id           |
| public.fly_ledger_entries.account_transaction_id           | public.account_transactions.account_transaction_id   |
| public.guest_book_entries.restaurant_id                    | public.restaurants.restaurant_id                     |
| public.guest_book_entries.user_id                          | public.users.user_id                                 |
| public.incentive_reads.user_id                             | public.users.user_id                                 |
| public.location_ai_data.location_id                        | public.locations.location_id                         |
| public.location_summaries.neighborhood_id                  | public.neighborhoods.neighborhood_id                 |
| public.locations.neighborhood_id                           | public.neighborhoods.neighborhood_id                 |
| public.locations.restaurant_id                             | public.restaurants.restaurant_id                     |
| public.locations.square_token_id                           | square.tokens.token_id                               |
| public.locations.supergood_toast_credential_id             | supergood_toast.credentials.credential_id            |
| public.locations_aud.rev                                   | public.revinfo.rev                                   |
| public.media.restaurant_id                                 | public.restaurants.restaurant_id                     |
| public.media_promotions.media_id                           | public.media.media_id                                |
| public.membership_events.membership_id                     | public.memberships.membership_id                     |
| public.membership_events.membership_tier_id                | public.membership_tiers.membership_tier_id           |
| public.memberships.membership_tier_id                      | public.membership_tiers.membership_tier_id           |
| public.memberships.nft_id                                  | public.nfts.nft_id                                   |
| public.memberships.restaurant_id                           | public.restaurants.restaurant_id                     |
| public.memberships.user_id                                 | public.users.user_id                                 |
| public.nfc_chips.restaurant_id                             | public.restaurants.restaurant_id                     |
| public.nfts.nft_airdrop_batch_id                           | public.nft_airdrop_batches.nft_airdrop_batch_id      |
| public.nfts.owner_user_id                                  | public.users.user_id                                 |
| public.nfts.restaurant_id                                  | public.restaurants.restaurant_id                     |
| public.open_hours.location_id                              | public.locations.location_id                         |
| public.opentable_guests.location_id                        | public.locations.location_id                         |
| public.opentable_guests.user_id                            | public.users.user_id                                 |
| public.passes.collaboration_id                             | public.collaborations.collaboration_id               |
| public.passes.nft_id                                       | public.nfts.nft_id                                   |
| public.passes.user_id                                      | public.users.user_id                                 |
| public.passes_aud.rev                                      | public.revinfo.rev                                   |
| public.pay_settings.user_id                                | public.users.user_id                                 |
| public.payment_links.payee_account_balance_id              | public.account_balances.account_balance_id           |
| public.payments.original_payment_id                        | public.payments.payment_id                           |
| public.payments.user_id                                    | public.users.user_id                                 |
| public.payout_accounts.restaurant_id                       | public.restaurants.restaurant_id                     |
| public.payouts.payout_account_id                           | public.payout_accounts.payout_account_id             |
| public.payouts.restaurant_id                               | public.restaurants.restaurant_id                     |
| public.ppx_entries.membership_tier_id                      | public.membership_tiers.membership_tier_id           |
| public.private_dining_rooms.card_id                        | public.cards.card_id                                 |
| public.private_dining_rooms.location_id                    | public.locations.location_id                         |
| public.private_dining_rooms.payment_link_id                | public.payment_links.payment_link_id                 |
| public.private_dining_rooms.restaurant_user_id             | public.restaurant_users.restaurant_user_id           |
| public.promotion_applications.promotion_redemption_id      | public.promotion_redemptions.promotion_redemption_id |
| public.promotion_codes.coupon_id                           | public.coupons.coupon_id                             |
| public.promotion_codes.user_id                             | public.users.user_id                                 |
| public.promotion_redemptions.promotion_code_id             | public.promotion_codes.promotion_code_id             |
| public.promotion_redemptions.user_id                       | public.users.user_id                                 |
| public.referral_codes.recipient_reward_rule_id             | public.reward_rules.reward_rule_id                   |
| public.referral_codes.restaurant_id                        | public.restaurants.restaurant_id                     |
| public.referral_codes.user_id                              | public.users.user_id                                 |
| public.referrals.code                                      | public.referral_codes.code                           |
| public.referrals.recipient_user_id                         | public.users.user_id                                 |
| public.referrals.restaurant_id                             | public.restaurants.restaurant_id                     |
| public.referrals.sender_user_id                            | public.users.user_id                                 |
| public.refunds.check_share_id                              | public.check_shares.check_share_id                   |
| public.refunds.payout_id                                   | public.payouts.payout_id                             |
| public.reservation_requests.location_id                    | public.locations.location_id                         |
| public.reservation_requests.reservation_id                 | public.reservations.reservation_id                   |
| public.reservation_requests.user_id                        | public.users.user_id                                 |
| public.reservations.location_id                            | public.locations.location_id                         |
| public.reservations.user_id                                | public.users.user_id                                 |
| public.restaurant_events.restaurant_id                     | public.restaurants.restaurant_id                     |
| public.restaurant_list_entries.list_id                     | public.restaurant_lists.list_id                      |
| public.restaurant_list_entries.restaurant_id               | public.restaurants.restaurant_id                     |
| public.restaurant_list_entries.user_id                     | public.users.user_id                                 |
| public.restaurant_lists.user_id                            | public.users.user_id                                 |
| public.restaurant_master_keys.restaurant_id                | public.restaurants.restaurant_id                     |
| public.restaurant_recommendations.location_id              | public.locations.location_id                         |
| public.restaurant_recommendations.restaurant_id            | public.restaurants.restaurant_id                     |
| public.restaurant_recommendations.user_id                  | public.users.user_id                                 |
| public.restaurant_user_integrations.restaurant_user_id     | public.restaurant_users.restaurant_user_id           |
| public.restaurant_users.user_id                            | public.users.user_id                                 |
| public.restaurant_users_locations.location_id              | public.locations.location_id                         |
| public.restaurant_users_locations.restaurant_user_id       | public.restaurant_users.restaurant_user_id           |
| public.restaurants.restaurant_group_id                     | public.restaurant_groups.restaurant_group_id         |
| public.restaurants_cuisines.cuisine_id                     | public.cuisines.cuisine_id                           |
| public.restaurants_cuisines.restaurant_id                  | public.restaurants.restaurant_id                     |
| public.reward_listings.restaurant_id                       | public.restaurants.restaurant_id                     |
| public.reward_listings.reward_rule_id                      | public.reward_rules.reward_rule_id                   |
| public.reward_rules.collaboration_id                       | public.collaborations.collaboration_id               |
| public.reward_rules.membership_tier_id                     | public.membership_tiers.membership_tier_id           |
| public.reward_rules.target_membership_tier_id              | public.membership_tiers.membership_tier_id           |
| public.reward_rules.target_reward_rule_id                  | public.reward_rules.reward_rule_id                   |
| public.rewards.check_in_id                                 | public.check_ins.check_in_id                         |
| public.rewards.reward_rule_id                              | public.reward_rules.reward_rule_id                   |
| public.rewards.user_id                                     | public.users.user_id                                 |
| public.scheduled_gift_emails.sender_user_id                | public.users.user_id                                 |
| public.subscription_terms.pass_id                          | public.passes.pass_id                                |
| public.subscription_terms.payment_id                       | public.payments.payment_id                           |
| public.user_cuisine_category_scores.cuisine_category_id    | public.cuisine_categories.cuisine_category_id        |
| public.user_cuisine_category_scores.user_id                | public.users.user_id                                 |
| public.user_devices.user_id                                | public.users.user_id                                 |
| public.user_incentive_activities.user_incentive_id         | public.user_incentives.user_incentive_id             |
| public.user_incentives.incentive_id                        | public.incentives.incentive_id                       |
| public.user_incentives.user_id                             | public.users.user_id                                 |
| public.user_media_views.media_id                           | public.media.media_id                                |
| public.user_media_views.user_id                            | public.users.user_id                                 |
| public.user_notifications.location_id                      | public.locations.location_id                         |
| public.user_notifications.user_id                          | public.users.user_id                                 |
| public.user_preferences.user_id                            | public.users.user_id                                 |
| public.user_price_scores.user_id                           | public.users.user_id                                 |
| public.user_status_overrides.status_id                     | public.statuses.status_id                            |
| public.user_status_overrides.user_id                       | public.users.user_id                                 |
| public.user_status_progress.user_id                        | public.users.user_id                                 |
| public.user_statuses.status_id                             | public.statuses.status_id                            |
| public.user_statuses.user_id                               | public.users.user_id                                 |
| public.user_statuses_aud.rev                               | public.revinfo.rev                                   |
| public.user_tags.user_id                                   | public.users.user_id                                 |
| public.user_terms.user_id                                  | public.users.user_id                                 |
| public.user_wallets.user_id                                | public.users.user_id                                 |
| public.users_aud.rev                                       | public.revinfo.rev                                   |
| public.users_neighborhoods_scores.neighborhood_id          | public.neighborhoods.neighborhood_id                 |
| public.users_neighborhoods_scores.user_id                  | public.users.user_id                                 |
| public.waitlist_entries.user_id                            | public.users.user_id                                 |
| square.orders.location_id                                  | public.locations.location_id                         |
| square.payments.location_id                                | public.locations.location_id                         |
| square.transactions.location_id                            | public.locations.location_id                         |
| supergood_toast.checks.location_id                         | public.locations.location_id                         |
| toast.export_configs.location_id                           | public.locations.location_id                         |
| toast.order_records.location_id                            | public.locations.location_id                         |

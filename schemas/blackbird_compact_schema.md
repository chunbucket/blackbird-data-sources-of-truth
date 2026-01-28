# Blackbird Production Database Schema

PostgreSQL 14.12 - Use this for query generation

## checkout

### sessions

id:int[PK], payload → acs → authentication_type:text, payload → acs → challenge_cancel_reason:text, payload → acs → challenge_cancel_reason_code:text, payload → acs → challenge_mandated:boolean, payload → acs → operator_id:text, payload → acs → reference_number:text, payload → acs → transaction_id:text, payload → acs → url:text, payload → amount:decimal, payload → approved:boolean, payload → authentication_category:text, payload → authentication_date:text, payload → authentication_type:text, payload → body:text, payload → cardholder_info:text, payload → certificates → ds_public:text, payload → challenged:boolean, payload → challenge_indicator:text, payload → cryptogram:text, payload → currency:text, payload → ds → ds_id:text, payload → ds → reference_number:text, payload → ds → transaction_id:text, payload → eci:text, payload → exemption → applied:text, payload → exemption → requested:text, payload → exemption → trusted_beneficiary → source:text, payload → exemption → trusted_beneficiary → status:text, payload → flow_type:text, payload → http_status_code:decimal, payload → id:text, payload → links → failure_url → href:text, payload → links → self → href:text, payload → links → success_url → href:text, payload → next_actions:text, payload → protocol_version:text, payload → reference:text, payload → request_id:text, payload → response_code:text, payload → response_headers → Cko-Client-Id:text, payload → response_headers → Cko-Correlation-Id:text, payload → response_headers → Cko-Request-Id:text, payload → response_headers → Cko-Session-Source:text, payload → response_headers → Cko-Version:text, payload → response_headers → Connection:text, payload → response_headers → Content-Length:text, payload → response_headers → Content-Type:text, payload → response_headers → Date:text, payload → response_headers → Strict-Transport-Security:text, payload → response_status_reason:text, payload → scheme:text, payload → self_link → href:text, payload → session_secret:text, payload → status:text, payload → status_reason:text, payload → transaction_id:text, payload → transaction_type:text, payload → xid:text, session_id:uuid, external_session_id:text, external_payment_id:text, payload:jsonb, created_at:tstz, updated_at:tstz

## gtm

### fly_contract_drops

id:int[PK], restaurant_group_id:uuid, allocation_fly:numeric

### icp_restaurants

zipcode:text, icp_restaurants:int

## hubspot

### deals

id:int[PK], properties → bbx:text, properties → bbx_category:text, properties → borough:text, properties → churn_details:text, properties → closed_lost:text, properties → closed_lost_details:text, properties → closed_lost_reason:text, properties → date_of_trial_end:text, properties → days_to_close:text, properties → deal_interest_areas:text, properties → deal_scope:text, properties → deal_source_details:text, properties → dealtype:text, properties → demo_date:text, properties → description:text, properties → end_of_trial_date:text, properties → fly_amount:text, properties → fly_matched:text, properties → hubspot_owner_assigneddate:text, properties → hubspot_team_id:text, properties → initial_deal:text, properties → last_touch:text, properties → new_deal_scope:text, properties → notes_last_contacted:ts, properties → notes_last_updated:ts, properties → notes_next_activity_date:text, properties → onboarding_contact_email:text, properties → onboarding_contact_nam:text, properties → onboarding_stall_details:text, properties → onboarding_stall_reasons:text, properties → pass_fee:text, properties → pass_group:text, properties → payments_live_date:text, properties → postal_code:text, properties → processing_months_free:text, properties → rating:text, properties → restaurant_name:text, properties → sdr:text, properties → transaction_fee:text, properties → win_reasons:text, external_id:text, close_date:tstz, create_date:tstz, deal_name:text, deal_stage:text, last_modified_date:tstz, pipeline:text, external_created_at:tstz, external_updated_at:tstz, created_at:tstz, updated_at:tstz, pass_sale_type:text, owner_id:text, account_onboarding_owner_id:text, reservation_platform:text, pos_system:text, google_places_id:text, amount:numeric, deal_source:text, live_date:date, churn_date:date, churn_reason:text, tier:text, market:text, properties:jsonb

### owners

id:int[PK], external_id:text, email:varchar, first_name:varchar, last_name:varchar, user_id:bigint, archived:bool, external_created_at:tstz, external_updated_at:tstz, created_at:tstz, updated_at:tstz

## public

### account_balance_snapshots

id:int[PK], snapshot_id:uuid, snapshot_timestamp:tstz, account_owner_type:text, account_owner_id:uuid, balance:numeric, account_updated_at:tstz, airdrop_batch_id:uuid, user_wallet_id:uuid

### account_balances

id:int[PK], account_balance_id:uuid, owner_type:text, owner_id:uuid, currency:text, balance:numeric, created_at:tstz, updated_at:tstz, treasury_prime_account_id:text, version:int

### account_balances_aud

id:int[PK], rev:int→revinfo.rev, revtype:int2, balance:numeric, created_at:tstz

### account_transactions

id:int[PK], account_transaction_id:uuid, origin_type:text, origin_id:uuid, created_at:tstz, updated_at:tstz, blackbird_payment_id:uuid→blackbird_payments.blackbird_payment_id

### activation_events

id:int[PK], activation_event_id:uuid[PK], location_id:uuid→locations.location_id, description:text, start_date:ts, end_date:ts, created_at:tstz, updated_at:tstz

### addresses

id:uuid[PK], nonce:numeric, address:text, chain_type:text

### adjustments

id:int[PK], adjustment_id:uuid, amount:bigint, fly_amount:bigint, house_account_amount:bigint, usd_amount:bigint, currency:text, check_share_id:uuid→check_shares.check_share_id, reason:text, comment:text, status:text, external_id:text, provider:text, payout_id:uuid→payouts.payout_id, created_at:tstz, updated_at:tstz

### banking_person_application_forms

id:int[PK], banking_person_application_form_id:uuid, restaurant_user_id:uuid→restaurant_users.restaurant_user_id, first_name:text, last_name:text, email_address:text, treasury_prime_person_application_id:text, created_at:tstz, updated_at:tstz

### billing_addresses

id:int[PK], billing_address_id:uuid, user_id:uuid→users.user_id, street:text, street2:text, city:text, state:text, zipcode:text, created_at:tstz, updated_at:tstz, country:text

### blackbird_payments

id:int[PK], blackbird_payment_id:uuid, user_id:uuid→users.user_id, item_id:uuid, item_type:text, card_id:uuid, card_type:text, card_payment_id:uuid→payments.payment_id, promotion_code_id:uuid→promotion_codes.promotion_code_id, discount_total:bigint, card_total:bigint, wallet_total:bigint, house_account_total:bigint, fly_total:bigint, total:bigint, status:text, created_at:tstz, updated_at:tstz

### blockchain_deposit_requests

id:int[PK], signature_id:uuid, created_at:tstz, updated_at:tstz, status:text, block_hash:text, wallet_id:uuid, transaction_id:uuid, value_amount:numeric, deposit_request_id:uuid

### blockchain_fly_pay_requests

id:uuid[PK], signature_id:uuid, origin_id:uuid, origin_type:text, created_at:tstz, updated_at:tstz, status:text, wallet_id:uuid, spent_amount:numeric, transaction_id:uuid, mint_amount:numeric, purchase_origin_id:uuid, to_address:text

### blockchain_restaurant_location_contracts

id:uuid[PK], location_id:uuid, contract_id:uuid, transaction_id:uuid, address:text, owner_address:text, restaurant_owner_address:text, created_at:tstz, updated_at:tstz

### blockchain_transaction_requests

id:uuid[PK], created_at:tstz, max_fee_per_gas:numeric, raw_data:text, signed_data:text, transaction_id:uuid, base_fee:numeric, max_priority_fee_per_gas:numeric

### blockchain_transactions

id:uuid[PK], created_at:tstz, request_id:uuid, address_id:uuid, to_address:text, status:text, nonce:numeric, gas_limit:numeric, gas_used:numeric, transaction_hash:text, encoded_function:text, budget_action_id:uuid, chain_type:text, version:int, tx_type:text, native_value:numeric

### budget_manager_action

id:int[PK], budget_action_id:uuid, worker_name:text, worker_table:text, runs_per_day:numeric

### budget_manager_config

id:int[PK], last_budget_update:tstz, profile_name:text, daily_spend_target:numeric, maximum_overspend_percent:numeric, current_budget:numeric

### cards

id:int[PK], card_id:uuid, user_id:uuid→users.user_id, provider:text, token:text, status:text, expiration_month:int, expiration_year:int, brand:text, last4:text, bin:text, card_type:text, card_category:text, issuer_country:text, product_id:text, product_type:text, is_default:bool, cardholder_name:text, expires_at:tstz, created_at:tstz, updated_at:tstz, billing_address_id:uuid→billing_addresses.billing_address_id, fingerprint:text, wallet_type:text, zipcode:text, authorization_external_payment_id:text, display_name:text

### check_ins

id:int[PK], check_in_id:uuid, nfc_chip_id:uuid→nfc_chips.nfc_chip_id, user_id:uuid→users.user_id, created_at:tstz, updated_at:tstz, restaurant_id:uuid→restaurants.restaurant_id, membership_id:uuid→memberships.membership_id, location_id:uuid, restaurant_visit_count:int, entry_id:uuid, ended_at:tstz, payment_funnel_type:text, initiation_type:text, hidden_at:tstz, \_created_at_edt:ts, intent_step_seen:bool

### check_shares

id:int[PK], check_share_id:uuid, check_id:uuid→checks.check_id, user_id:uuid→users.user_id, payment_method_id:uuid→cards.card_id, house_account_fly_credit:numeric, check_share_total:bigint, gratuity_preference_value:bigint, gratuity_preference_type:text, created_at:tstz, updated_at:tstz, is_party_host:bool, check_in_id:uuid→check_ins.check_in_id, gratuity:bigint, apply_fly_balance:bool, fly_credit:numeric, user_identifying_order_item_provider_id:uuid, service_charges:bigint

### check_shares_aud

id:int[PK], rev:int→revinfo.rev, revtype:int2, payment_method_id:uuid, created_at:tstz

### checks

id:int[PK], check_id:uuid, pos_provider_id:uuid, pos_provider:text, status:text, created_at:tstz, updated_at:tstz, party_size:bigint, total:bigint, sub_total:bigint, tax:bigint, discounts:bigint, due:bigint, gratuity:bigint, service_charges:bigint, other_charges:bigint, amount_paid:bigint, num_items:int, pos_provider_check_id:uuid, location_id:uuid→locations.location_id, payment_method_id:uuid→cards.card_id, payout_id:uuid→payouts.payout_id, webhook_updated_at:tstz, bb_payment_total:bigint, service_type:text, gratuity_value:bigint, gratuity_type:text, expires_at:tstz, bb_credit_total:bigint, payment_scenario:text, pos_provider_request_id:uuid, has_late_webhook:bool, table_number:text, in_store_code:varchar, check_number:text, prepayment:bigint, bb_fee_cents:bigint, closing_employee_id:uuid→employees.employee_id, paid_at:tstz

### checks_aud

id:int[PK], rev:int→revinfo.rev, revtype:int2, payment_method_id:uuid, created_at:tstz

### chits

id:int[PK], chit_id:uuid, user_id:uuid→users.user_id, internal_blurb:text, created_at:tstz, updated_at:tstz, external_blurb:text, blurb:text, internal_blurb_system_prompt:text, external_blurb_system_prompt:text, summary_blurb_system_prompt:text, hint:text

### city_zip_codes

id:int[PK], city_zip_code_id:uuid, zip_code:text, city:text, region:text

### collaboration_perks

collab_perk_id:uuid[PK], collaboration_id:uuid→collaborations.collaboration_id, title:text, description:text, id:int[PK], created_at:ts, updated_at:ts

### collaboration_restaurants

id:int[PK], collaboration_id:uuid→collaborations.collaboration_id, restaurant_id:uuid→restaurants.restaurant_id, created_at:tstz, updated_at:tstz

### collaborations

id:int[PK], collaboration_id:uuid, name:text, description:text, expiration_date:date, image:text, benefits:text, created_at:tstz, updated_at:tstz, artist:text, url:text, price_usd:bigint, email_template_id:text, payment_image:text, sale_start_date:date, sale_end_date:date, primary_region_id:uuid→regions.region_id, promo_description:text, expiration_type:text, expiration_period:text, state:text, active_start_time:time, active_end_time:time, waitlist_email_template_id:text, primary_reward:text, terms:text, renewable:bool, terms_full:text, slug:text, quantity_sold:int, max_quantity:int, unsubscribe_email_template_id:text, background_color:varchar, about:text, text_color:varchar, confirmation_email_image:text, confirmation_email_copy:text, waitlist_email_copy:text, level_2_sale_start_date:date, level_3_sale_start_date:date, level_4_sale_start_date:date

### combined_user_activities

created_at_edt:tstz, user_id:text, activity_id:text, checkin_type:text

### conversation_messages

id:int[PK], provider_id:text, conversation_id:int→conversations.id, author:text, author_type:text, author_participant_id:text, body:text, index:int, timestamp:tstz, created_at:tstz, updated_at:tstz

### conversations

id:int[PK], conversation_provider_id:text, location_id:uuid→locations.location_id, user_id:uuid→users.user_id, unique_name:text, conversation_type:text, created_at:tstz, updated_at:tstz, active:bool

### coupons

id:int[PK], coupon_id:uuid, amount_off:bigint, duration:text, duration_in_months:int, active:bool, max_redemptions:int, name:varchar, percent_off:float8, redeem_by:tstz, times_redeemed:int, created_at:tstz, updated_at:tstz, item_id:uuid, item_type:text, purchasable:bool

### cuisine_categories

id:int[PK], cuisine_category_id:uuid[PK], name:text, created_at:tstz, updated_at:tstz

### cuisines

id:int[PK], cuisine_id:uuid[PK], cuisine_category_id:uuid→cuisine_categories.cuisine_category_id, name:text, created_at:tstz, updated_at:tstz

### curated_recommendations

id:int[PK], curated_recommendation_id:uuid, region_id:uuid→regions.region_id, location_id:uuid→locations.location_id, category:text, month:int, year:int, created_at:tstz, updated_at:tstz

### employee_check_actions

id:int[PK], employee_id:uuid→employees.employee_id, check_id:uuid→checks.check_id, action:text, created_at:tstz, updated_at:tstz

### employee_incentive_progresses

id:int[PK], employee_incentive_progress_id:uuid, employee_id:uuid→employees.employee_id, employee_incentive_id:uuid→employee_incentives.employee_incentive_id, progress:int, created_at:tstz, updated_at:tstz

### employee_incentives

id:int[PK], employee_incentive_id:uuid, location_id:uuid→locations.location_id, starts_at:ts, ends_at:ts, created_at:ts, updated_at:ts, status:text, target:int, group_reward_cents:int, individual_reward_cents:int, completed_at:ts

### employee_pin_tokens

id:bigint[PK], token:text, employee_id:uuid→employees.employee_id, expires_at:tstz, created_at:tstz, updated_at:tstz

### employees

id:int[PK], user_id:uuid→users.user_id, location_id:uuid→locations.location_id, active:bool, created_at:tstz, updated_at:tstz, employee_id:uuid, last_active_at:tstz, pin:varchar

### evm_contracts

id:uuid[PK], contract_type:text, contract_address:text, deployer_address:text, implementation_address:text, abi:jsonb, bytecode:text, is_proxy:bool, deployed_at:tstz, created_at:tstz

### experiments

user_id:uuid, experiment:text, treatment:text, created_at:tstz, updated_at:tstz

### external_chit_payloads

user_id:uuid, first_name:text, last_name:text, email:text, birthdate:date, avatar:text, city:text, state_abbr:text

### f2_distribution_configs

id:int[PK], period_id:uuid, period_name:text, period_start:tstz, period_end:tstz, total_user_fly_throughput:numeric, total_restaurant_fly_throughput:numeric, f2_user_allocation:numeric, f2_restaurant_allocation:numeric, excluded_location_ids:\_text, claim_period_end_date:tstz

### f2_distributions

id:int[PK], distribution_id:uuid, created_at:tstz, fly_throughput_snapshot_id:uuid, account_owner_type:text, account_owner_id:uuid, distribution_amount:numeric, period_id:uuid, account_updated_at:tstz, rank:bigint

### failed_sessions

id:int[PK], failed_session_id:uuid, restaurant_id:uuid, location_id:uuid, nfc_chip_id:uuid, user_id:uuid→users.user_id, platform:text, error_code:text, reason:text, debug_message:text, created_at:tstz, updated_at:tstz

### fly_airdrop_batches

id:uuid[PK], snapshot_id:uuid, transaction_id:uuid, status:text, retry_count:int, airdrop_amount:numeric, created_at:tstz, updated_at:tstz

### fly_distribution_adjustments

id:int[PK], date:date, days_remaining:int, projected_issuance:numeric, actual_issuance:numeric, created_at:tstz, updated_at:tstz, total_future_issuance:numeric

### fly_ledger_entries

id:int[PK], fly_ledger_entry_id:uuid, origin_type:text, origin_id:uuid, credit_amount:numeric, created_at:tstz, updated_at:tstz, fly_multiplier:int, debit_amount:numeric, account_transaction_id:uuid→account_transactions.account_transaction_id, account_balance_id:uuid→account_balances.account_balance_id, balance_snapshot:numeric

### fly_purchase_requests

id:int[PK], fly_purchase_request_id:uuid, created_at:tstz, updated_at:tstz

### fly_throughput_snapshots

id:int[PK], fly_throughput_snapshot_id:uuid, created_at:tstz, account_owner_type:text, account_owner_id:uuid, account_updated_at:tstz, account_balance:numeric, debits:numeric, total_velocity:numeric, period_id:uuid

### flyway_schema_history

installed_rank:int[PK], version:varchar, description:varchar, type:varchar, script:varchar, checksum:int, installed_by:varchar, installed_on:ts, execution_time:int, success:bool

### geography_columns

f_table_catalog:name, f_table_schema:name, f_table_name:name, f_geography_column:name, coord_dimension:int, srid:int, type:text

### geometry_columns

f_table_catalog:varchar, f_table_schema:name, f_table_name:name, f_geometry_column:name, coord_dimension:int, srid:int, type:varchar

### guest_book_entries

id:int[PK], restaurant_id:uuid→restaurants.restaurant_id, user_id:uuid→users.user_id, phone_number:text, visits:int, guest_notes:text, vip:bool, created_at:tstz, updated_at:tstz

### image_urls

id:int[PK], url:text, created_at:tstz, updated_at:tstz

### incentive_reads

user_id:uuid→users.user_id, last_read_at:ts, updated_at:ts, created_at:ts

### incentives

id:int[PK], reward_configuration → statusReward → statusId:text, threshold → dineThreshold:decimal, threshold → minimumSpend:decimal, threshold → referralThreshold:decimal, threshold → spendThreshold:decimal, incentive_id:uuid, type:text, title:text, description:text, image:text, threshold:jsonb, start_time:ts, end_time:ts, expiration_period:text, expiration_type:text, eligible_cohorts:jsonb, fly_reward:numeric, created_at:ts, updated_at:ts, terms:text, notification_title:text, notification_body:text, notification_route_url:text, in_app_message:text, accepted_currencies:jsonb, eligible_location_ids:jsonb, reward_configuration:jsonb, eligibility:text, rewards:jsonb, eligible_restaurant_ids:jsonb

### internal_chit_payloads

user_id:uuid, first_name:text, last_name:text, tip_percentage:text, fsr_spender_label:text, qsr_spender_label:text, last_three_label:text, neighborhood_label:text, frequency_label:text, fly_balance_label:text, avg_tip_pct_raw:numeric, avg_fsr_spend:numeric, avg_qsr_spend:numeric, visits_per_week:numeric, fly_balance:numeric, city:text, state_abbr:text, avatar:text

### internal_chit_payloads_mv

user_id:uuid, first_name:text, last_name:text, tip_percentage:text, fsr_spender_label:text, qsr_spender_label:text, last_three_label:text, neighborhood_label:text, frequency_label:text, fly_balance_label:text, avg_tip_pct_raw:numeric, avg_fsr_spend:numeric, avg_qsr_spend:numeric, visits_per_week:numeric, fly_balance:numeric, city:text, state_abbr:text, avatar:text

### ipfs_snapshots

id:int[PK], pin_cid:text, transaction_id:uuid, batch_cutoff:tstz

### jobrunr_backgroundjobservers

id:bpchar[PK], workerpoolsize:int, pollintervalinseconds:int, firstheartbeat:ts, lastheartbeat:ts, running:int, systemtotalmemory:bigint, systemfreememory:bigint, systemcpuload:numeric, processmaxmemory:bigint, processfreememory:bigint, processallocatedmemory:bigint, processcpuload:numeric, deletesucceededjobsafter:varchar, permanentlydeletejobsafter:varchar, name:varchar

### jobrunr_jobs

id:bpchar[PK], version:int, jobasjson:text, jobsignature:varchar, state:varchar, createdat:ts, updatedat:ts, scheduledat:ts, recurringjobid:varchar

### jobrunr_jobs_stats

total:bigint, awaiting:bigint, scheduled:bigint, enqueued:bigint, processing:bigint, failed:bigint, succeeded:bigint, alltimesucceeded:numeric, deleted:bigint, nbrofbackgroundjobservers:bigint, nbrofrecurringjobs:bigint

### jobrunr_metadata

id:varchar[PK], name:varchar, owner:varchar, value:text, createdat:ts, updatedat:ts

### jobrunr_migrations

id:bpchar[PK], script:varchar, installedon:varchar

### jobrunr_recurring_jobs

id:bpchar[PK], version:int, jobasjson:text, createdat:bigint

### launch_info

id:int[PK], platform:text, app_name:text, minimum_app_version:text, current_app_version:text, created_at:tstz, updated_at:tstz, latest_terms_version:date

### location_ai_data

location_id:uuid→locations.location_id, recommended_items:\_text, description:text, created_at:ts, updated_at:ts, what_to_know:\_text, restaurant_id:varchar, reservation_url:varchar, instagram_url:varchar

### location_summaries

id:int[PK], date:date, neighborhood_id:uuid→neighborhoods.neighborhood_id, live:int, payments_enabled:int, created_at:tstz, updated_at:tstz

### location_weekly_reports

check_in_summary → last_week:decimal, check_in_summary → repeat:decimal, check_in_summary → this_week:decimal, location_id:uuid, membership_summary → last_week:decimal, membership_summary → this_week:decimal, payment_volume_summary → last_week:decimal, payment_volume_summary → this_week:decimal, payment_volume_summary → total_savings:decimal, restaurant_id:uuid, location_name:text, restaurant_name:text, two_weeks_ago:date, one_week_ago:date, today:date, membership_summary:json, check_in_summary:json, payment_volume_summary:json, top_user_ids:\_uuid

### locations

id:int[PK], location_id:uuid, restaurant_id:uuid→restaurants.restaurant_id, name:text, messaging_country_code:text, messaging_phone_number:text, street:text, street2:text, city:text, state:text, zipcode:text, country:text, created_at:tstz, updated_at:tstz, wifi_ssid:text, wifi_password:text, time_zone:text, coordinate:geometry, rooam_pos_id:uuid, payments_enabled:bool, opentable_id:text, opentable_external_id:uuid, neighborhood_id:uuid→neighborhoods.neighborhood_id, reservation_url:text, live:bool, google_place_id:text, open_hours_last_synced_at:tstz, open_hours_override:bool, is_billable:bool, accepts_prepayment:bool, requires_employee_pin:bool, sandbox_enabled_at:tstz, square_merchant_id:text, square_token_id:uuid→tokens.token_id, blackbird_fee_bips:int, use_square_sidecar:bool, resy_token_id:uuid, resy_venue_id:int, is_club:bool, service_charge_bips:int, google_maps_rating:float8, create_landing_page:bool, service_charge_frequency:text, sidecar_configurable:bool, auto_gratuity_enabled:bool, pos_type:text, slug:text, employee_incentive_cadence:text, employee_incentive_target:int, has_sidecar_table_number:bool, has_sidecar_check_number:bool, employee_incentive_group_reward_cents:int, employee_incentive_individual_reward_cents:int, square_location_id:text, supergood_toast_credential_id:uuid→credentials.credential_id

### locations_aud

id:int[PK], rev:int→revinfo.rev, revtype:int2, payments_enabled:bool, created_at:tstz, coordinate:geometry

### locations_updates

location_id:uuid, id:int[PK], last_payments_enabled:tstz, last_coordinate:tstz

### media

id:int[PK], media_id:uuid, restaurant_id:uuid→restaurants.restaurant_id, file_type:text, title:text, url:text, created_at:tstz, updated_at:tstz, file_extension:text

### media_promotions

id:int[PK], media_promotion_id:uuid[PK], media_id:uuid→media.media_id, start_date_time:tstz, end_date_time:tstz, created_at:tstz, updated_at:tstz

### membership_events

id:int[PK], membership_id:uuid→memberships.membership_id, membership_tier_id:uuid→membership_tiers.membership_tier_id, event_type:text, event_source:text, event_source_id:uuid, created_at:tstz, updated_at:tstz

### membership_tiers

id:int[PK], membership_tier_id:uuid, access_level:int, name:text, active:bool, created_at:tstz, updated_at:tstz, quantity:int, term_value:int, term_unit:text, artist:text, image:text, restaurant_id:uuid, renewable:bool, about_copy:text, how_it_works_copy:text, benefits_copy:text, messaging_enabled:bool, quantity_remaining:int, confirmation_email_copy:text, confirmation_email_header_copy:text, price_usd:bigint, image_preview:text, image_full:text, image_web:text

### memberships

id:int[PK], membership_id:uuid, user_id:uuid→users.user_id, nft_id:uuid→nfts.nft_id, acquisition_source:text, acquisition_source_id:uuid, status:text, created_at:tstz, updated_at:tstz, membership_tier_id:uuid→membership_tiers.membership_tier_id, restaurant_id:uuid→restaurants.restaurant_id, total_fly:numeric, check_in_count:int, last_check_in_date:tstz, referral_count:int, messaging_enabled:bool

### menu_option_sets

id:int[PK], menu_option_set_id:uuid, name:text, minimum_selections:int, required:bool, created_at:tstz, updated_at:tstz, version:bigint

### neighborhood_zipcodes

id:int[PK], neighborhood_name:text, zipcode_int:text, created_at:ts, updated_at:ts, zipcode:text, city:text, state_abbr:text, state_name:text, zcta:bool, zcta_parent:text, population:int, density:numeric, county_code_primary:text, county_name:text, county_weights:jsonb, official_county_names:text, official_county_code:text, imprecise:bool, military:bool, time_zone:text, geo_point:geometry, latitude:numeric, longitude:numeric, country_code:varchar, households_200k_plus_pct:numeric, housing_units:int, households:int, avg_income:int, median_income:int

### neighborhoods

id:int[PK], neighborhood_id:uuid, name:text, city:text, created_at:tstz, updated_at:tstz

### nfc_chips

id:int[PK], nfc_chip_id:uuid, restaurant_id:uuid→restaurants.restaurant_id, action:text, created_at:tstz, updated_at:tstz, table_number:text, location_id:uuid, read_ctr:numeric

### nft_airdrop_batches

id:int[PK], nft_airdrop_batch_id:uuid, transaction_id:uuid, status:text, quantity_airdropped:int, created_at:tstz, updated_at:tstz

### nft_mint_batches

id:uuid[PK], created_at:tstz, updated_at:tstz, transaction_id:uuid, nft_contract_address:text, status:text, starting_token_id:numeric, quantity_minted:int

### nft_supply_counts

id:int[PK], contract_address:text, total_minted:numeric

### nfts

id:int[PK], nft_id:uuid, created_at:tstz, updated_at:tstz, token_id:numeric, owner_address:text, owner_user_id:uuid→users.user_id, metadata_url:text, status:text, restaurant_id:uuid→restaurants.restaurant_id, contract_address:text, nft_airdrop_batch_id:uuid→nft_airdrop_batches.nft_airdrop_batch_id

### open_hours

id:int[PK], location_id:uuid→locations.location_id, day_of_week:text, start_time:time, end_time:time, created_at:tstz, updated_at:tstz

### opentable_guests

id:int[PK], user_id:uuid→users.user_id, location_id:uuid→locations.location_id, venue_guest_id:text, created_at:ts, updated_at:ts

### passes

id:int[PK], pass_id:uuid, user_id:uuid→users.user_id, collaboration_id:uuid→collaborations.collaboration_id, nft_id:uuid→nfts.nft_id, acquisition_source:text, acquisition_source_id:uuid, created_at:tstz, updated_at:tstz, state:text, expires_at:tstz, visit_count:int, restaurants_visited:int, auto_renew:bool

### passes_aud

id:int[PK], rev:int→revinfo.rev, revtype:int2, state:text, auto_renew:bool

### pay_settings

id:int[PK], user_id:uuid→users.user_id, default_tip_percent:int, default_pay_with_fly:bool, hide_check_settings_page:bool, created_at:ts, updated_at:ts

### payment_links

id:int[PK], payment_link_id:uuid, payee_account_balance_id:uuid→account_balances.account_balance_id, amount_cents:bigint, description:text, expires_at:tstz, created_at:tstz, updated_at:tstz, paid_at:tstz

### payments

id:int[PK], payment_id:uuid, external_id:text, user_id:uuid→users.user_id, provider:text, currency:text, amount:bigint, status:text, created_at:tstz, updated_at:tstz, item_type:text, item_id:uuid, original_payment_id:uuid→payments.payment_id, payment_method_type:text, payment_method_id:uuid, provider_response_code:text, refund_amount:bigint

### payout_accounts

id:int[PK], payout_account_id:uuid, provider:text, provider_id:text, restaurant_id:uuid→restaurants.restaurant_id, created_at:tstz, updated_at:tstz, location_id:uuid

### payouts

id:int[PK], payout_id:uuid, period_end_time:tstz, status:text, total_check_amount:bigint, bb_fee_bips:bigint, bb_fee_amount:bigint, net_payout_amount:bigint, restaurant_id:uuid→restaurants.restaurant_id, payout_account_id:uuid→payout_accounts.payout_account_id, created_at:tstz, updated_at:tstz, location_id:uuid, provider_id:text, total_adjustment_amount:bigint, total_due_amount:bigint, external_bill_id:varchar, bb_transaction_fee_amount:bigint

### pg_stat_statements

userid:oid, dbid:oid, toplevel:bool, queryid:bigint, query:text, plans:bigint, total_plan_time:float8, min_plan_time:float8, max_plan_time:float8, mean_plan_time:float8, stddev_plan_time:float8, calls:bigint, total_exec_time:float8, min_exec_time:float8, max_exec_time:float8, mean_exec_time:float8, stddev_exec_time:float8, rows:bigint, shared_blks_hit:bigint, shared_blks_read:bigint, shared_blks_dirtied:bigint, shared_blks_written:bigint, local_blks_hit:bigint, local_blks_read:bigint, local_blks_dirtied:bigint, local_blks_written:bigint, temp_blks_read:bigint, temp_blks_written:bigint, blk_read_time:float8, blk_write_time:float8, wal_records:bigint, wal_fpi:bigint, wal_bytes:numeric

### pg_stat_statements_info

dealloc:bigint, stats_reset:tstz

### popular_restaurants_view

id:bigint[PK], region_id:uuid, restaurant_id:uuid, name:text, score:int, cohort:text, is_bb1:bool

### ppx_entries

id:int[PK], ppx_entry_id:uuid, restaurant_id:uuid, membership_tier_id:uuid→membership_tiers.membership_tier_id, phone_number:text, email:text, full_name:text, created_at:tstz, updated_at:tstz

### press_checks_backup

check_id:uuid, created_at:tstz

### private_dining_rooms

id:bigint[PK], pdr_id:uuid, location_id:uuid→locations.location_id, restaurant_user_id:uuid→restaurant_users.restaurant_user_id, customer_email:varchar, event_description:text, deposit_amount_cents:bigint, final_charge_amount_cents:bigint, status:text, payment_link_id:uuid→payment_links.payment_link_id, card_id:uuid→cards.card_id, requires_card_on_file:bool, deposit_paid_at:tstz, final_charge_processed_at:tstz, created_at:tstz, updated_at:tstz, event_date:tstz

### promo_codes

id:int[PK], promo_code_id:uuid, product_type:text, product_id:uuid, discount_type:text, discount_value:bigint, code:varchar, active:bool, created_at:ts, updated_at:ts

### promotion_applications

id:int[PK], promotion_application_id:uuid, promotion_redemption_id:uuid→promotion_redemptions.promotion_redemption_id, item_id:uuid, item_type:text, created_at:tstz, updated_at:tstz

### promotion_codes

id:int[PK], promotion_code_id:uuid, active:bool, code:varchar, expires_at:tstz, max_redemptions:int, times_redeemed:int, coupon_id:uuid→coupons.coupon_id, created_at:tstz, updated_at:tstz, user_id:uuid→users.user_id, acquisition_source:text, acquisition_source_id:uuid

### promotion_redemptions

id:int[PK], promotion_redemption_id:uuid, starts_at:tstz, ends_at:tstz, promotion_code_id:uuid→promotion_codes.promotion_code_id, user_id:uuid→users.user_id, created_at:tstz, updated_at:tstz

### ranked_fly_throughput_view

account_owner_type:text, account_owner_id:uuid, account_updated_at:tstz, account_balance:numeric, debits:numeric, total_velocity:numeric, rank:bigint, account_balance_id:int, account_balance_uuid:uuid, period_id:uuid

### referral_codes

id:int[PK], code:text, user_id:uuid→users.user_id, restaurant_id:uuid→restaurants.restaurant_id, active:bool, created_at:tstz, updated_at:tstz, recipient_reward_rule_id:uuid→reward_rules.reward_rule_id, sender_reward_usd:bigint, sender_alias:text

### referrals

id:int[PK], referral_id:uuid, sender_user_id:uuid→users.user_id, recipient_user_id:uuid→users.user_id, restaurant_id:uuid→restaurants.restaurant_id, code:text→referral_codes.code, state:text, created_at:tstz, updated_at:tstz

### refunds

id:int[PK], refund_id:uuid, amount:bigint, currency:text, check_share_id:uuid→check_shares.check_share_id, refund_reason:text, comment:text, refund_status:text, external_id:text, provider:text, payout_id:uuid→payouts.payout_id, created_at:tstz, updated_at:tstz, fly_amount:bigint, house_account_amount:bigint, usd_amount:bigint

### regions

id:int[PK], region_id:uuid, name:text, center:geometry, radius:float8, active:bool, created_at:tstz, updated_at:tstz, time_zone:text

### reservation_requests

id:int[PK], reservation_request_id:uuid, user_id:uuid→users.user_id, location_id:uuid→locations.location_id, reservation_id:uuid→reservations.reservation_id, state:text, party_size:int, request_dates:jsonb, request_start_time:time, request_end_time:time, created_at:tstz, updated_at:tstz, platform:text

### reservations

id:int[PK], provider_type:text, user_id:uuid→users.user_id, location_id:uuid→locations.location_id, server_name:text, table_number:text, party_size:int, reservation_time:tstz, external_id:text, state:text, created_at:tstz, updated_at:tstz, external_updated_at:tstz, seated_at:ts, reservation_id:uuid, notified_at:ts

### restaurant_attributes

restaurant_id:uuid, attribute_type:text, attribute_value:text, created_at:tstz, updated_at:tstz

### restaurant_events

id:int[PK], event_id:uuid, restaurant_id:uuid→restaurants.restaurant_id, event_type:text, created_at:tstz, updated_at:tstz

### restaurant_groups

id:int[PK], restaurant_group_id:uuid, name:text, created_at:tstz, updated_at:tstz

### restaurant_list_entries

id:int[PK], list_id:uuid→restaurant_lists.list_id, restaurant_id:uuid→restaurants.restaurant_id, user_id:uuid→users.user_id, created_at:tstz, updated_at:tstz

### restaurant_lists

id:int[PK], list_id:uuid, user_id:uuid→users.user_id, list_type:text, custom_name:text, created_at:tstz, updated_at:tstz

### restaurant_master_keys

id:int[PK], restaurant_id:uuid→restaurants.restaurant_id, master_key_hex:text, created_at:tstz, updated_at:tstz

### restaurant_recommendations

id:int[PK], restaurant_recommendation_id:uuid, user_id:uuid→users.user_id, location_id:uuid→locations.location_id, restaurant_id:uuid→restaurants.restaurant_id, category:text, created_at:tstz, updated_at:tstz

### restaurant_user_integrations

id:int[PK], restaurant_user_id:uuid→restaurant_users.restaurant_user_id, provider:text, access_token:text, access_token_updated_at:tstz, created_at:tstz, metadata:text

### restaurant_users

id:int[PK], restaurant_user_id:uuid, user_id:uuid→users.user_id, email:text, chat_identity:text, created_at:tstz, updated_at:tstz, show_accounting_tab:bool

### restaurant_users_locations

id:int[PK], restaurant_user_id:uuid→restaurant_users.restaurant_user_id, location_id:uuid→locations.location_id, created_at:tstz, updated_at:tstz, receives_payout_email:bool, restaurant_user_location_id:uuid

### restaurants

id:int[PK], restaurant_id:uuid, name:text, created_at:tstz, updated_at:tstz, restaurant_group_id:uuid→restaurant_groups.restaurant_group_id, image:text, reporting_enabled:bool, cuisine:text, reward_mode:text, cohort:text, has_messaging_enabled:bool, website_url:text, price:text, score:int, instagram_url:text, tiktok_url:text, recommended_items:varchar, image_preview:text, image_web:text, image_full:text, image_background_color:text

### restaurants_cuisines

id:int[PK], cuisine_id:uuid→cuisines.cuisine_id, restaurant_id:uuid→restaurants.restaurant_id, created_at:tstz, updated_at:tstz

### revinfo

rev:int[PK], revtstmp:bigint

### reward_listings

id:int[PK], reward_listing_id:uuid, reward_rule_id:uuid→reward_rules.reward_rule_id, restaurant_id:uuid→restaurants.restaurant_id, price_fly:numeric, quantity:int, quantity_remaining:int, active:bool, created_at:tstz, updated_at:tstz

### reward_rules

id:int[PK], reward_rule_id:uuid, restaurant_id:uuid, check_in_threshold:int, emoji:text, label:text, description:text, created_at:tstz, updated_at:tstz, internal_label:text, internal_description:text, target_membership_tier_id:uuid→membership_tiers.membership_tier_id, active:bool, duration:int, metadata:text, membership_tier_id:uuid→membership_tiers.membership_tier_id, collaboration_id:uuid→collaborations.collaboration_id, fly_reward:numeric, is_upcoming:bool, target_reward_rule_id:uuid→reward_rules.reward_rule_id, image:text, is_visible_consumer:bool, is_visible_restaurant:bool, auto_redeemed:bool, fly_reward_bips:int

### rewards

id:int[PK], origin_type:text, origin_id:uuid, reward_id:uuid, reward_rule_id:uuid→reward_rules.reward_rule_id, user_id:uuid→users.user_id, created_at:tstz, updated_at:tstz, expires_at:tstz, membership_id:uuid, state:text, check_in_id:uuid→check_ins.check_in_id

### scheduled_gift_emails

id:int[PK], payment_id:uuid, account_transaction_id:uuid, sender_user_id:uuid→users.user_id, recipient_name:text, recipient_email:text, send_at:tstz, status:text, created_at:tstz, updated_at:tstz

### scheduled_worker_runs

id:uuid[PK], worker_name:text, started_at:tstz, last_completed_at:tstz, last_processed_id:bigint, state:text, run_count:bigint, max_run_duration_seconds:numeric

### service_configurations

id:int[PK], key:text[PK], value:text, created_at:ts, updated_at:ts, service_name:text

### statuses

id:int[PK], status_id:uuid, name:text, level:int, description:text, fly_multiplier:int, fly_deposit_threshold:numeric, spend_threshold:int, check_in_threshold:int, year_start:int, year_end:int, created_at:tstz, updated_at:tstz, max_reservation_requests:int, track:text, benefits:jsonb, title:text, byline:text, disclaimers:jsonb, nft_status_id:int, image_url:text

### subscription_terms

id:int[PK], subscription_term_id:uuid, pass_id:uuid→passes.pass_id, payment_id:uuid→payments.payment_id, starts_at:tstz, renews_at:tstz, created_at:tstz, updated_at:tstz, status:text

### sun_data_entries

id:int[PK], entry_id:uuid, user_id:uuid, cmac:text, picc_data:text, read_ctr:int, created_at:tstz, updated_at:tstz

### temp_darsh_loctions

location_id:text, reservation_url:text, restaurant_id:text, instagram_url:text, what_to_know:text, recommended_items:text, id_location:text, id_restaurant:text

### user_cuisine_category_scores

id:int[PK], cuisine_category_id:uuid→cuisine_categories.cuisine_category_id, user_id:uuid→users.user_id, check_in_count:int, created_at:tstz, updated_at:tstz

### user_devices

id:int[PK], user_device_id:uuid, user_id:uuid→users.user_id, platform:text, version:text, created_at:tstz, updated_at:tstz, user_agent:text

### user_incentive_activities

user_incentive_activity_id:uuid, user_incentive_id:uuid→user_incentives.user_incentive_id, activity_type:text, activity_id:uuid, spend_amount:numeric, created_at:tstz, updated_at:tstz

### user_incentives

id:int[PK], user_incentive_id:uuid, incentive_id:uuid→incentives.incentive_id, user_id:uuid→users.user_id, status:text, expires_at:ts, completed_at:ts, created_at:ts, updated_at:ts, current_progress:numeric, enrolled_at:tstz

### user_media_views

id:int[PK], user_media_view_id:uuid[PK], user_id:uuid→users.user_id, media_id:uuid→media.media_id, created_at:tstz, updated_at:tstz

### user_notifications

id:int[PK], user_notification_id:uuid, user_id:uuid→users.user_id, location_id:uuid→locations.location_id, entity_type:text, entity_id:uuid, message_body:text, read_at:tstz, created_at:tstz, updated_at:tstz

### user_preferences

id:int[PK], user_id:uuid→users.user_id, data_sharing_enabled:bool, created_at:tstz, updated_at:tstz, default_tip_percentage:int, learn_blackbird:bool, learn_fly:bool

### user_price_scores

id:int[PK], user_id:uuid→users.user_id, price:text, check_in_count:int, created_at:tstz, updated_at:tstz

### user_status_overrides

id:int[PK], user_id:uuid→users.user_id, status_id:uuid→statuses.status_id, starts_at:tstz, ends_at:tstz, created_at:tstz, updated_at:tstz, origin_id:uuid, origin_type:text

### user_status_progress

id:int[PK], user_id:uuid→users.user_id, year:int, check_ins:int, spend:int, fly_deposit:numeric, created_at:tstz, updated_at:tstz, user_status_progress_id:uuid

### user_statuses

id:int[PK], user_status_id:uuid, user_id:uuid→users.user_id, status_id:uuid→statuses.status_id, state:text, started_at:tstz, ended_at:tstz, created_at:tstz, updated_at:tstz

### user_statuses_aud

id:int[PK], rev:int→revinfo.rev, revtype:int2, state:text

### user_tags

id:int[PK], user_tag_id:uuid, user_id:uuid→users.user_id, type:user_tag_type, metadata:jsonb, created_at:tstz, updated_at:tstz

### user_terms

id:int[PK], user_id:uuid→users.user_id, version:date, platform:text, app_name:text, created_at:tstz, updated_at:tstz

### user_wallet_permits

id:int[PK], wallet_permit_id:uuid, signature_id:uuid, transaction_id:uuid, status:text, user_id:uuid, user_wallet_id:uuid, currency:text, created_at:tstz, updated_at:tstz

### user_wallets

id:int[PK], user_wallet_id:uuid, user_id:uuid→users.user_id, wallet_type:text, address:text, provider_index:int, created_at:tstz, updated_at:tstz

### users

id:int[PK], user_id:uuid, first_name:text, last_name:text, phone_number:text, country_code:text, created_at:tstz, updated_at:tstz, email:text, zipcode:text, birthdate:date, fly_multiplier:int, avatar:text, active:bool, chat_identity:text, discord:text, wallet_provider_id:text, account_status:text, internal:bool

### users_aud

id:int[PK], rev:int→revinfo.rev, revtype:int2, phone_number:text, fly_multiplier:int, active:bool, account_status:text, created_at:tstz

### users_neighborhoods_scores

id:int[PK], user_id:uuid→users.user_id, neighborhood_id:uuid→neighborhoods.neighborhood_id, check_in_count:int, created_at:tstz, updated_at:tstz

### waitlist_entries

id:int[PK], email:text, first_name:text, last_name:text, target_id:uuid, target_type:text, created_at:tstz, updated_at:tstz, user_id:uuid→users.user_id

### wallet_signatures

id:int[PK], signature_id:uuid, created_at:tstz, updated_at:tstz, is_active:bool, entity_id:uuid, wallet_id:uuid, from_address:text, to_address:text, value_amount:numeric, valid_after:text, valid_before:text, nonce:text, signature:text, chain_id:numeric, contract_name:text, verifying_contract_address:text, owner:text, spender:text, deadline:text, function_name:text

### webhook_events

id:int[PK], payload → created_at:ts, payload → created_on:ts, payload → data → balances → available_to_capture:decimal, payload → data → balances → total_authorized:decimal, payload → data → currency:text, payload → data → customer → email:text, payload → data → eci:text, payload → data → event_links → payment_actions:text, payload → data → object → order_created → created_at:ts, payload → data → object → order_created → location_id:text, payload → data → object → order_created → order_id:text, payload → data → object → order_created → state:text, payload → data → object → order_updated → created_at:ts, payload → data → object → order_updated → order_id:text, payload → data → object → order_updated → state:text, payload → data → object → order_updated → updated_at:ts, payload → data → object → order_updated → version:decimal, payload → data → object → payment → amount_money → currency:text, payload → data → object → payment → app_fee_money → amount:decimal, payload → data → object → payment → app_fee_money → currency:text, payload → data → object → payment → application_details → application_id:text, payload → data → object → payment → approved_money → currency:text, payload → data → object → payment → billing_address → address_line_1:text, payload → data → object → payment → billing_address → country:text, payload → data → object → payment → billing_address → first_name:text, payload → data → object → payment → billing_address → locality:text, payload → data → object → payment → billing_address → postal_code:text, payload → data → object → payment → card_details → application_cryptogram:text, payload → data → object → payment → card_details → application_identifier:text, payload → data → object → payment → card_details → auth_result_code:text, payload → data → object → payment → card_details → avs_status:text, payload → data → object → payment → card_details → card → card_brand:text, payload → data → object → payment → card_details → card → exp_year:decimal, payload → data → object → payment → card_details → card → fingerprint:text, payload → data → object → payment → card_details → card → last_4:text, payload → data → object → payment → card_details → card → payment_account_reference:text, payload → data → object → payment → card_details → card_payment_timeline → authorized_at:ts, payload → data → object → payment → card_details → card_payment_timeline → captured_at:ts, payload → data → object → payment → card_details → cvv_status:text, payload → data → object → payment → card_details → device_details → device_installation_id:text, payload → data → object → payment → card_details → device_details → device_name:text, payload → data → object → payment → card_details → emv_details → authorization_response_code:text, payload → data → object → payment → card_details → statement_description:text, payload → data → object → payment → card_details → verification_method:text, payload → data → object → payment → card_details → verification_results:text, payload → data → object → payment → cash_details → buyer_supplied_money → amount:decimal, payload → data → object → payment → customer_id:text, payload → data → object → payment → delay_duration:text, payload → data → object → payment → device_details → device_id:text, payload → data → object → payment → external_details → source:text, payload → data → object → payment → external_details → type:text, payload → data → object → payment → location_id:text, payload → data → object → payment → order_id:text, payload → data → object → payment → receipt_url:text, payload → data → object → payment → risk_evaluation → created_at:ts, payload → data → object → payment → shipping_address → first_name:text, payload → data → object → payment → source_type:text, payload → data → object → payment → tip_money → amount:decimal, payload → data → object → payment → total_money → amount:decimal, payload → data → pan_type_processed:text, payload → data → payment_account_reference:text, payload → data → processed_on:text, payload → data → processing → acquirer_reference_number:text, payload → data → processing → acquirer_transaction_id:text, payload → data → processing → aft:text, payload → data → processing → card_acceptor_id:text, payload → data → processing_channel_id:text, payload → data → processing → partner_response_code:text, payload → data → processing → retrieval_reference_number:text, payload → data → processing → scheme:text, payload → data → processing → scheme_merchant_id:text, payload → data → reference:text, payload → data → response_code:text, payload → data → response_summary:text, payload → data → scheme_id:text, payload → data → source → account_holder → account_name_inquiry:text, payload → data → source → account_holder → account_name_inquiry_details → first_name:text, payload → data → source → account_holder → last_name:text, payload → data → source → account_holder → type:text, payload → data → source → billing_address → country:text, payload → data → source → billing_address → state:text, payload → data → source → billing_address → town_city:text, payload → data → source → billing_address → zip:text, payload → data → source → card_wallet_type:text, payload → data → source → cvv_check:text, payload → data → source → fingerprint:text, payload → data → source → issuer:text, payload → data → source → last_4:text, payload → data → source → local_schemes:text, payload → data → source → product_id:text, payload → data → source → product_type:text, payload → data → source → type:text, payload → data → type:text, payload → event_id:text, payload → id:text, payload → \_links → payment → href:text, payload → \_links → refund → href:text, payload → merchant_id:text, payload → type:text, payload → version:text, webhook_event_id:uuid, route:text, payload:jsonb, created_at:tstz, updated_at:tstz

## square

### orders

id:int[PK], payload → closed_at:ts, payload → created_at:ts, payload → customer_id:text, payload → discounts:text, payload → fulfillments:text, payload → id:text, payload → line_items:text, payload → location_id:text, payload → net_amount_due_money → amount:decimal, payload → net_amount_due_money → currency:text, payload → net_amounts → card_surcharge_money → amount:decimal, payload → net_amounts → card_surcharge_money → currency:text, payload → net_amounts → discount_money → amount:decimal, payload → net_amounts → discount_money → currency:text, payload → net_amounts → service_charge_money → amount:decimal, payload → net_amounts → service_charge_money → currency:text, payload → net_amounts → tax_money → amount:decimal, payload → net_amounts → tax_money → currency:text, payload → net_amounts → tip_money → amount:decimal, payload → net_amounts → tip_money → currency:text, payload → net_amounts → total_money → amount:decimal, payload → net_amounts → total_money → currency:text, payload → pricing_options → auto_apply_discounts:boolean, payload → pricing_options → auto_apply_taxes:boolean, payload → reference_id:text, payload → rewards:text, payload → source → name:text, payload → state:text, payload → taxes:text, payload → tenders:text, payload → ticket_name:text, payload → total_card_surcharge_money → amount:decimal, payload → total_card_surcharge_money → currency:text, payload → total_discount_money → amount:decimal, payload → total_discount_money → currency:text, payload → total_money → amount:decimal, payload → total_money → currency:text, payload → total_service_charge_money → amount:decimal, payload → total_service_charge_money → currency:text, payload → total_tax_money → amount:decimal, payload → total_tax_money → currency:text, payload → total_tip_money → amount:decimal, payload → total_tip_money → currency:text, payload → updated_at:ts, payload → version:decimal, order_id:uuid, location_id:uuid→locations.location_id, external_id:text, payload:jsonb, created_at:tstz, updated_at:tstz

### payments

id:int[PK], payment_id:uuid, location_id:uuid→locations.location_id, external_id:text, payload:jsonb, created_at:tstz, updated_at:tstz

### tokens

id:int[PK], token_id:uuid, access_token:text, refresh_token:text, created_at:tstz, updated_at:tstz

### transactions

id:int[PK], transaction_id:uuid, location_id:uuid→locations.location_id, external_transaction_id:text, date:date, time:time, time_zone:text, gross_sales:bigint, discounts:bigint, service_charges:bigint, net_sales:bigint, gift_card_sales:bigint, tax:bigint, tip:bigint, partial_refunds:bigint, total_collected:bigint, source:text, card:bigint, card_entry_method:text, square_gift_card:bigint, other_tender:bigint, other_tender_type:text, fees:bigint, net_total:bigint, payment_id:text, card_brand:text, pan_suffix:text, device_name:text, staff_name:text, staff_id:text, details:text, description:text, event_type:text, external_location:text, dining_option:text, customer_id:text, customer_name:text, customer_reference_id:text, device_nickname:text, third_party_fees:bigint, deposit_id:text, deposit_date:text, deposit_details:text, fee_percentage:text, fee_fixed_rate:text, refund_reason:text, discount_name:text, transaction_status:text, cash_app:bigint, order_reference_id:text, fulfillment_note:text, free_processing_applied:bigint, in_store_code:text, created_at:tstz, updated_at:tstz

## supergood_toast

### checks

id:int[PK], payload → guestFeedback:text, payload → payments:text, payload → pricing → amount:text, payload → pricing → amountDue:text, payload → pricing → appliedDiscounts:text, payload → pricing → currency:text, payload → pricing → taxAmount:text, payload → pricing → tipAmount:text, payload → pricing → tipPercentage:decimal, payload → pricing → totalAmount:text, payload → selections:text, check_id:uuid, location_id:uuid→locations.location_id, external_id:uuid, external_order_id:uuid, payload:jsonb, created_at:tstz, updated_at:tstz

### credentials

id:int[PK], credential_id:uuid, username:text, password:text, auth_token:text, created_at:tstz, updated_at:tstz

## toast

### export_configs

id:int[PK], export_config_id:uuid, username:text, server_url:text, export_id:int, is_active:bool, location_id:uuid→locations.location_id, updated_at:ts, created_at:ts

### order_records

id:int[PK], order_record_id:uuid, payment_id:text, location_id:uuid→locations.location_id, order_number:int, order_date:tstz, tab_name:text, server:text, table_name:text, dining_area:text, service:text, dining_option:text, amount:numeric, tip:numeric, gratuity:numeric, total:numeric, void_date:tstz, other_type:text, processed_at:tstz, created_at:tstz, updated_at:tstz, type:text, card_type:text

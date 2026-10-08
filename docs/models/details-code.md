# DetailsCode

## Example Usage

```typescript
import { DetailsCode } from "@clientcasa/sdk/models";

let value: DetailsCode = "status_changed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"impersonation_write_refused" | "archived_record_read_only" | "paused_transaction_window_locked" | "expense_recognition_period_sealed" | "record_has_dependents" | "duplicate_record" | "record_immutable" | "quota_exceeded" | "invalid_payload" | "timeline_operation_expired" | "unknown_client_email" | "already_in_state" | "status_settled" | "status_changed" | "document_issued" | "document_settings_locked" | "setup_retry_limit" | "signing_setup_needs_attention" | "global_mode_has_assignments" | "unsupported_file_type" | "file_too_large" | "cross_organization" | "linked_record_not_found" | "linked_records_multiple_organizations" | "rate_limited" | "revenue_on_internal_project" | "number_series_unlocked" | "invoice_not_deletable" | "invoice_not_closable" | "sale_not_deletable" | "receipt_not_deletable" | "email_send_blocked" | "tax_category_default" | "tax_category_referenced" | "recipe_price_propagation_failed" | "price_history_head_mismatch" | "price_history_not_derived" | "time_entry_already_billed" | "charge_period_already_billed" | "owner_immutable" | "payment_client_mismatch" | "payment_target_not_collectible" | "payment_origin_invoice_unlicensed" | "payment_origin_invoice_mismatch" | "currency_locked" | "event_day_companion_write_failed" | "timeline_anchor_missing" | "document_companion_write_failed" | "timeline_companion_write_failed" | "payment_companion_write_failed" | "payout_companion_write_failed" | "transaction_companion_write_failed" | "record_companion_write_failed" | "schedule_companion_write_failed" | "platform_companion_write_failed" | "smart_file_not_sent_yet" | "smart_file_not_out_with_client" | "already_billing_contact" | "send_door_required" | "receipt_door_required" | "outbox_organization_frozen" | "unknown_assignment_id" | Unrecognized<string>
```
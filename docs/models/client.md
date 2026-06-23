# Client

## Example Usage

```typescript
import { Client } from "@clientcasa/sdk/models";

let value: Client = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  status: "active",
  notes: null,
  taxSettings: {
    defaultTaxable: false,
    overrideTaxRate: false,
    taxRate: 3892.41,
  },
  invoiceRemindersEnabled: false,
  attachInvoicePdf: true,
  attachReceiptPdf: false,
  recurringBilling: {
    status: "pending_setup",
    nextBillingDate: new Date("2026-06-09"),
  },
  sourceSubmissionId: "550e8400-e29b-41d4-a716-446655440000",
  createdAt: new Date("2024-12-12T02:49:22.743Z"),
  updatedAt: new Date("2026-12-09T17:03:44.747Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | [models.ClientStatus](../models/client-status.md)                                             | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `notes`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `taxSettings`                                                                                 | [models.ClientTaxSettings](../models/client-tax-settings.md)                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `invoiceRemindersEnabled`                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `attachInvoicePdf`                                                                            | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `attachReceiptPdf`                                                                            | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `recurringBilling`                                                                            | [models.RecurringBilling](../models/recurring-billing.md)                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `sourceSubmissionId`                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
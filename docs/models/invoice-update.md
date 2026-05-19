# InvoiceUpdate

## Example Usage

```typescript
import { InvoiceUpdate } from "@clientcasa/sdk/models";

let value: InvoiceUpdate = {
  billingContactId: "550e8400-e29b-41d4-a716-446655440000",
  projectIds: [
    "550e8400-e29b-41d4-a716-446655440000",
  ],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `billingContactId`                                               | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `projectIds`                                                     | *string*[]                                                       | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `status`                                                         | [models.InvoiceUpdateStatus](../models/invoice-update-status.md) | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `subject`                                                        | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `issueDate`                                                      | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `dueDate`                                                        | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `paymentTerms`                                                   | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `notes`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
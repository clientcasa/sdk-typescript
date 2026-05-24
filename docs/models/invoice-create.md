# InvoiceCreate

## Example Usage

```typescript
import { InvoiceCreate } from "@clientcasa/sdk/models";

let value: InvoiceCreate = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  billingContactId: "550e8400-e29b-41d4-a716-446655440000",
  projectIds: [
    "550e8400-e29b-41d4-a716-446655440000",
  ],
  lineItems: [
    {
      description: "easy yowza a unlike rim horde sparse huzzah",
      quantity: 8298.99,
      unitPrice: 6845.35,
    },
  ],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `clientId`                                                       | *string*                                                         | :heavy_check_mark:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `billingContactId`                                               | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `projectIds`                                                     | *string*[]                                                       | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `status`                                                         | [models.InvoiceCreateStatus](../models/invoice-create-status.md) | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `subject`                                                        | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `issueDate`                                                      | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `dueDate`                                                        | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `paymentTerms`                                                   | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `notes`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `lineItems`                                                      | [models.LineItem](../models/line-item.md)[]                      | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
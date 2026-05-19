# UpdateInvoiceRequest

## Example Usage

```typescript
import { UpdateInvoiceRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateInvoiceRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    billingContactId: "550e8400-e29b-41d4-a716-446655440000",
    projectIds: [
      "550e8400-e29b-41d4-a716-446655440000",
    ],
  },
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            | Example                                                |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `id`                                                   | *string*                                               | :heavy_check_mark:                                     | UUID v4                                                | 550e8400-e29b-41d4-a716-446655440000                   |
| `body`                                                 | [models.InvoiceUpdate](../../models/invoice-update.md) | :heavy_check_mark:                                     | N/A                                                    |                                                        |
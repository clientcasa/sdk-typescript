# CreateInvoiceRequest

## Example Usage

```typescript
import { CreateInvoiceRequest } from "@clientcasa/sdk/models/operations";

let value: CreateInvoiceRequest = {
  idempotencyKey: "create-client-2026-05-24-a1b2c3",
  body: {
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
  },
};
```

## Fields

| Field                                                                                                                                                                                                       | Type                                                                                                                                                                                                        | Required                                                                                                                                                                                                    | Description                                                                                                                                                                                                 | Example                                                                                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                                                                                                                            | *string*                                                                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                                                                          | Optional unique key that makes this create safely retryable. Replaying the same key returns the original response instead of creating a duplicate; reusing a key with a different request body returns 409. | create-client-2026-05-24-a1b2c3                                                                                                                                                                             |
| `body`                                                                                                                                                                                                      | [models.InvoiceCreate](../../models/invoice-create.md)                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                          | N/A                                                                                                                                                                                                         |                                                                                                                                                                                                             |
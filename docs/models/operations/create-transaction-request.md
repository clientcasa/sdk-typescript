# CreateTransactionRequest

## Example Usage

```typescript
import { CreateTransactionRequest } from "@clientcasa/sdk/models/operations";

let value: CreateTransactionRequest = {
  idempotencyKey: "create-client-2026-05-24-a1b2c3",
  body: {
    name: "<value>",
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
    taxCategoryId: "550e8400-e29b-41d4-a716-446655440000",
    amount: 2654.98,
    direction: "cost",
    assignments: [
      {
        projectId: "550e8400-e29b-41d4-a716-446655440000",
        clientId: "550e8400-e29b-41d4-a716-446655440000",
      },
    ],
  },
};
```

## Fields

| Field                                                                                                                                                                                                       | Type                                                                                                                                                                                                        | Required                                                                                                                                                                                                    | Description                                                                                                                                                                                                 | Example                                                                                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                                                                                                                            | *string*                                                                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                                                                          | Optional unique key that makes this create safely retryable. Replaying the same key returns the original response instead of creating a duplicate; reusing a key with a different request body returns 409. | create-client-2026-05-24-a1b2c3                                                                                                                                                                             |
| `body`                                                                                                                                                                                                      | [models.TransactionCreate](../../models/transaction-create.md)                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                          | N/A                                                                                                                                                                                                         |                                                                                                                                                                                                             |
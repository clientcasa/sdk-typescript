# UpdateTransactionRequest

## Example Usage

```typescript
import { UpdateTransactionRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateTransactionRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  idempotencyKey: "create-client-2026-05-24-a1b2c3",
  body: {
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
    taxCategoryId: "550e8400-e29b-41d4-a716-446655440000",
    assignments: [
      {
        id: "68b9e3d1c4a2f70012ab34cd",
        projectId: "550e8400-e29b-41d4-a716-446655440000",
        clientId: "550e8400-e29b-41d4-a716-446655440000",
      },
    ],
  },
};
```

## Fields

| Field                                                                                                                                                                                                        | Type                                                                                                                                                                                                         | Required                                                                                                                                                                                                     | Description                                                                                                                                                                                                  | Example                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                                                         | *string*                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                           | UUID v4                                                                                                                                                                                                      | 550e8400-e29b-41d4-a716-446655440000                                                                                                                                                                         |
| `idempotencyKey`                                                                                                                                                                                             | *string*                                                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                           | Optional unique key that makes this request safely retryable. Replaying the same key returns the original response instead of creating a duplicate; reusing a key with a different request body returns 409. | create-client-2026-05-24-a1b2c3                                                                                                                                                                              |
| `body`                                                                                                                                                                                                       | [models.TransactionUpdate](../../models/transaction-update.md)                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                                           | N/A                                                                                                                                                                                                          |                                                                                                                                                                                                              |
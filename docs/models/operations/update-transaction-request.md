# UpdateTransactionRequest

## Example Usage

```typescript
import { UpdateTransactionRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateTransactionRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
    taxCategoryId: "550e8400-e29b-41d4-a716-446655440000",
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

| Field                                                          | Type                                                           | Required                                                       | Description                                                    | Example                                                        |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `id`                                                           | *string*                                                       | :heavy_check_mark:                                             | UUID v4                                                        | 550e8400-e29b-41d4-a716-446655440000                           |
| `body`                                                         | [models.TransactionUpdate](../../models/transaction-update.md) | :heavy_check_mark:                                             | N/A                                                            |                                                                |
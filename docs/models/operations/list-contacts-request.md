# ListContactsRequest

## Example Usage

```typescript
import { ListContactsRequest } from "@clientcasa/sdk/models/operations";

let value: ListContactsRequest = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        | Example                                            |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `page`                                             | *number*                                           | :heavy_minus_sign:                                 | N/A                                                |                                                    |
| `pageSize`                                         | *number*                                           | :heavy_minus_sign:                                 | N/A                                                |                                                    |
| `clientId`                                         | *string*                                           | :heavy_minus_sign:                                 | UUID v4                                            | 550e8400-e29b-41d4-a716-446655440000               |
| `role`                                             | [operations.Role](../../models/operations/role.md) | :heavy_minus_sign:                                 | N/A                                                |                                                    |
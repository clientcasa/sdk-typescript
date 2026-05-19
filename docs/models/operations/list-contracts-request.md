# ListContractsRequest

## Example Usage

```typescript
import { ListContractsRequest } from "@clientcasa/sdk/models/operations";

let value: ListContractsRequest = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
| `clientId`                                                                         | *string*                                                                           | :heavy_minus_sign:                                                                 | UUID v4                                                                            | 550e8400-e29b-41d4-a716-446655440000                                               |
| `status`                                                                           | [operations.ListContractsStatus](../../models/operations/list-contracts-status.md) | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
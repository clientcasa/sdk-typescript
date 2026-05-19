# ListProposalsRequest

## Example Usage

```typescript
import { ListProposalsRequest } from "@clientcasa/sdk/models/operations";

let value: ListProposalsRequest = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
| `clientId`                                                                         | *string*                                                                           | :heavy_minus_sign:                                                                 | UUID v4                                                                            | 550e8400-e29b-41d4-a716-446655440000                                               |
| `status`                                                                           | [operations.ListProposalsStatus](../../models/operations/list-proposals-status.md) | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
| `archived`                                                                         | *boolean*                                                                          | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
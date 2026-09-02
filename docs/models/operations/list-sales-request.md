# ListSalesRequest

## Example Usage

```typescript
import { ListSalesRequest } from "@clientcasa/sdk/models/operations";

let value: ListSalesRequest = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  businessId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                | Example                                                                    |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `page`                                                                     | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `pageSize`                                                                 | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `status`                                                                   | [operations.ListSalesStatus](../../models/operations/list-sales-status.md) | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `channel`                                                                  | [operations.Channel](../../models/operations/channel.md)                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `clientId`                                                                 | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `businessId`                                                               | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `saleDateFrom`                                                             | [Date](../../types/rfcdate.md)                                             | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `saleDateTo`                                                               | [Date](../../types/rfcdate.md)                                             | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
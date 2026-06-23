# ListVendorsRequest

## Example Usage

```typescript
import { ListVendorsRequest } from "@clientcasa/sdk/models/operations";

let value: ListVendorsRequest = {
  categoryId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    | Example                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `page`                                                                         | *number*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |                                                                                |
| `pageSize`                                                                     | *number*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |                                                                                |
| `categoryId`                                                                   | *string*                                                                       | :heavy_minus_sign:                                                             | UUID v4                                                                        | 550e8400-e29b-41d4-a716-446655440000                                           |
| `status`                                                                       | [operations.ListVendorsStatus](../../models/operations/list-vendors-status.md) | :heavy_minus_sign:                                                             | N/A                                                                            |                                                                                |
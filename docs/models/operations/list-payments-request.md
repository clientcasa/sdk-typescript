# ListPaymentsRequest

## Example Usage

```typescript
import { ListPaymentsRequest } from "@clientcasa/sdk/models/operations";

let value: ListPaymentsRequest = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  invoiceId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      | Example                                                                          |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `page`                                                                           | *number*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |                                                                                  |
| `pageSize`                                                                       | *number*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |                                                                                  |
| `clientId`                                                                       | *string*                                                                         | :heavy_minus_sign:                                                               | UUID v4                                                                          | 550e8400-e29b-41d4-a716-446655440000                                             |
| `invoiceId`                                                                      | *string*                                                                         | :heavy_minus_sign:                                                               | UUID v4                                                                          | 550e8400-e29b-41d4-a716-446655440000                                             |
| `status`                                                                         | [operations.ListPaymentsStatus](../../models/operations/list-payments-status.md) | :heavy_minus_sign:                                                               | N/A                                                                              |                                                                                  |
| `kind`                                                                           | [operations.ListPaymentsKind](../../models/operations/list-payments-kind.md)     | :heavy_minus_sign:                                                               | N/A                                                                              |                                                                                  |
# PaymentCreate

## Example Usage

```typescript
import { PaymentCreate } from "@clientcasa/sdk/models";

let value: PaymentCreate = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  invoiceId: "550e8400-e29b-41d4-a716-446655440000",
  amount: 8515.4,
  receivedDate: new Date("2025-05-08"),
  method: "bank_transfer",
  refundOfId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `clientId`                                                       | *string*                                                         | :heavy_check_mark:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `invoiceId`                                                      | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `amount`                                                         | *number*                                                         | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
| `currency`                                                       | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `receivedDate`                                                   | [Date](../types/rfcdate.md)                                      | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
| `method`                                                         | [models.PaymentCreateMethod](../models/payment-create-method.md) | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
| `kind`                                                           | [models.PaymentCreateKind](../models/payment-create-kind.md)     | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `reference`                                                      | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `notes`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `refundOfId`                                                     | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
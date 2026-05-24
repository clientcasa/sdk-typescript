# ListPaymentsResponse

## Example Usage

```typescript
import { ListPaymentsResponse } from "@clientcasa/sdk/models/operations";

let value: ListPaymentsResponse = {
  result: {
    data: [],
    pagination: {
      page: 299018,
      pageSize: 331897,
      total: 615983,
      totalPages: 226919,
      hasMore: true,
    },
  },
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `result`                                           | [models.PaymentList](../../models/payment-list.md) | :heavy_check_mark:                                 | N/A                                                |
# ListPayoutsResponse

## Example Usage

```typescript
import { ListPayoutsResponse } from "@clientcasa/sdk/models/operations";

let value: ListPayoutsResponse = {
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

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `result`                                         | [models.PayoutList](../../models/payout-list.md) | :heavy_check_mark:                               | N/A                                              |
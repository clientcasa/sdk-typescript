# ListPaymentsResponse

OK

## Example Usage

```typescript
import { ListPaymentsResponse } from "@clientcasa/sdk/models/operations";

let value: ListPaymentsResponse = {
  data: [],
  pagination: {
    page: 299018,
    pageSize: 331897,
    total: 615983,
    totalPages: 226919,
    hasMore: true,
  },
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `data`                                                   | [models.Payment](../../models/payment.md)[]              | :heavy_check_mark:                                       | N/A                                                      |
| `pagination`                                             | [models.PaginationMeta](../../models/pagination-meta.md) | :heavy_check_mark:                                       | N/A                                                      |
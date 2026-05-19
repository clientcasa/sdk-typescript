# ListTransactionsResponse

OK

## Example Usage

```typescript
import { ListTransactionsResponse } from "@clientcasa/sdk/models/operations";

let value: ListTransactionsResponse = {
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
| `data`                                                   | [models.Transaction](../../models/transaction.md)[]      | :heavy_check_mark:                                       | N/A                                                      |
| `pagination`                                             | [models.PaginationMeta](../../models/pagination-meta.md) | :heavy_check_mark:                                       | N/A                                                      |
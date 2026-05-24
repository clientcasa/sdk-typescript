# ListTransactionsResponse

## Example Usage

```typescript
import { ListTransactionsResponse } from "@clientcasa/sdk/models/operations";

let value: ListTransactionsResponse = {
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

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `result`                                                   | [models.TransactionList](../../models/transaction-list.md) | :heavy_check_mark:                                         | N/A                                                        |
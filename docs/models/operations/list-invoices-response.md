# ListInvoicesResponse

## Example Usage

```typescript
import { ListInvoicesResponse } from "@clientcasa/sdk/models/operations";

let value: ListInvoicesResponse = {
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
| `result`                                           | [models.InvoiceList](../../models/invoice-list.md) | :heavy_check_mark:                                 | N/A                                                |
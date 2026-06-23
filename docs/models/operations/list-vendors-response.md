# ListVendorsResponse

## Example Usage

```typescript
import { ListVendorsResponse } from "@clientcasa/sdk/models/operations";

let value: ListVendorsResponse = {
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
| `result`                                         | [models.VendorList](../../models/vendor-list.md) | :heavy_check_mark:                               | N/A                                              |
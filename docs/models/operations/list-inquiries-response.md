# ListInquiriesResponse

## Example Usage

```typescript
import { ListInquiriesResponse } from "@clientcasa/sdk/models/operations";

let value: ListInquiriesResponse = {
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
| `result`                                           | [models.InquiryList](../../models/inquiry-list.md) | :heavy_check_mark:                                 | N/A                                                |
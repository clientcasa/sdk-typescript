# ListContactsResponse

## Example Usage

```typescript
import { ListContactsResponse } from "@clientcasa/sdk/models/operations";

let value: ListContactsResponse = {
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
| `result`                                           | [models.ContactList](../../models/contact-list.md) | :heavy_check_mark:                                 | N/A                                                |
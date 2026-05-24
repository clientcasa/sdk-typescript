# ListClientsResponse

## Example Usage

```typescript
import { ListClientsResponse } from "@clientcasa/sdk/models/operations";

let value: ListClientsResponse = {
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
| `result`                                         | [models.ClientList](../../models/client-list.md) | :heavy_check_mark:                               | N/A                                              |
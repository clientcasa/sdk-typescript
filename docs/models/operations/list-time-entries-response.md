# ListTimeEntriesResponse

## Example Usage

```typescript
import { ListTimeEntriesResponse } from "@clientcasa/sdk/models/operations";

let value: ListTimeEntriesResponse = {
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

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `result`                                                | [models.TimeEntryList](../../models/time-entry-list.md) | :heavy_check_mark:                                      | N/A                                                     |
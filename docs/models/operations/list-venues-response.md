# ListVenuesResponse

## Example Usage

```typescript
import { ListVenuesResponse } from "@clientcasa/sdk/models/operations";

let value: ListVenuesResponse = {
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

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `result`                                       | [models.VenueList](../../models/venue-list.md) | :heavy_check_mark:                             | N/A                                            |
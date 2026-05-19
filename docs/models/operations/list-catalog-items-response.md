# ListCatalogItemsResponse

OK

## Example Usage

```typescript
import { ListCatalogItemsResponse } from "@clientcasa/sdk/models/operations";

let value: ListCatalogItemsResponse = {
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
| `data`                                                   | [models.CatalogItem](../../models/catalog-item.md)[]     | :heavy_check_mark:                                       | N/A                                                      |
| `pagination`                                             | [models.PaginationMeta](../../models/pagination-meta.md) | :heavy_check_mark:                                       | N/A                                                      |
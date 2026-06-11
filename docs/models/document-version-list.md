# DocumentVersionList

## Example Usage

```typescript
import { DocumentVersionList } from "@clientcasa/sdk/models";

let value: DocumentVersionList = {
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

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `data`                                                    | [models.DocumentVersion](../models/document-version.md)[] | :heavy_check_mark:                                        | N/A                                                       |
| `pagination`                                              | [models.PaginationMeta](../models/pagination-meta.md)     | :heavy_check_mark:                                        | N/A                                                       |
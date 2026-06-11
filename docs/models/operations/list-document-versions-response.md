# ListDocumentVersionsResponse

## Example Usage

```typescript
import { ListDocumentVersionsResponse } from "@clientcasa/sdk/models/operations";

let value: ListDocumentVersionsResponse = {
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

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `result`                                                            | [models.DocumentVersionList](../../models/document-version-list.md) | :heavy_check_mark:                                                  | N/A                                                                 |
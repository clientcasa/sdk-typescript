# ListClientDocumentsResponse

## Example Usage

```typescript
import { ListClientDocumentsResponse } from "@clientcasa/sdk/models/operations";

let value: ListClientDocumentsResponse = {
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

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `result`                                                          | [models.ClientDocumentList](../../models/client-document-list.md) | :heavy_check_mark:                                                | N/A                                                               |
# ListFormSubmissionsResponse

## Example Usage

```typescript
import { ListFormSubmissionsResponse } from "@clientcasa/sdk/models/operations";

let value: ListFormSubmissionsResponse = {
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
| `result`                                                          | [models.FormSubmissionList](../../models/form-submission-list.md) | :heavy_check_mark:                                                | N/A                                                               |
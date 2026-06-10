# ListFormsResponse

## Example Usage

```typescript
import { ListFormsResponse } from "@clientcasa/sdk/models/operations";

let value: ListFormsResponse = {
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

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `result`                                     | [models.FormList](../../models/form-list.md) | :heavy_check_mark:                           | N/A                                          |
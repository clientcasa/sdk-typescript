# ListWebhooksResponse

OK

## Example Usage

```typescript
import { ListWebhooksResponse } from "@clientcasa/sdk/models/operations";

let value: ListWebhooksResponse = {
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
| `data`                                                   | [models.Webhook](../../models/webhook.md)[]              | :heavy_check_mark:                                       | N/A                                                      |
| `pagination`                                             | [models.PaginationMeta](../../models/pagination-meta.md) | :heavy_check_mark:                                       | N/A                                                      |
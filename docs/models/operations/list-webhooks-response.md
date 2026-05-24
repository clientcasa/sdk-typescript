# ListWebhooksResponse

## Example Usage

```typescript
import { ListWebhooksResponse } from "@clientcasa/sdk/models/operations";

let value: ListWebhooksResponse = {
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

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `result`                                           | [models.WebhookList](../../models/webhook-list.md) | :heavy_check_mark:                                 | N/A                                                |
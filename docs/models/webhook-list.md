# WebhookList

## Example Usage

```typescript
import { WebhookList } from "@clientcasa/sdk/models";

let value: WebhookList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      name: "<value>",
      url: "https://infinite-pronoun.info/",
      events: [
        "payment_received",
      ],
      enabled: true,
      source: "make",
      hasSecret: true,
      lastTriggered: null,
      lastStatus: 970084,
      consecutiveFailures: 827526,
      createdAt: new Date("2026-11-04T12:24:33.184Z"),
      updatedAt: new Date("2024-11-06T19:49:14.398Z"),
    },
  ],
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

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `data`                                                | [models.Webhook](../models/webhook.md)[]              | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
# Webhook

## Example Usage

```typescript
import { Webhook } from "@clientcasa/sdk/models";

let value: Webhook = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  url: "https://sad-outlaw.org",
  events: [
    "lead_created",
  ],
  enabled: true,
  source: "n8n",
  hasSecret: false,
  lastTriggered: null,
  lastStatus: 358833,
  consecutiveFailures: 480602,
  createdAt: new Date("2026-10-09T23:01:39.726Z"),
  updatedAt: new Date("2025-09-25T16:57:49.249Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `events`                                                                                      | [models.WebhookEvent](../models/webhook-event.md)[]                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `enabled`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `source`                                                                                      | [models.WebhookSource](../models/webhook-source.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `hasSecret`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `lastTriggered`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `lastStatus`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `consecutiveFailures`                                                                         | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
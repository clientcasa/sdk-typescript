# WebhookCreate

## Example Usage

```typescript
import { WebhookCreate } from "@clientcasa/sdk/models";

let value: WebhookCreate = {
  name: "<value>",
  url: "https://nautical-grass.info",
  events: [],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `url`                                                            | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `events`                                                         | [models.WebhookCreateEvent](../models/webhook-create-event.md)[] | :heavy_check_mark:                                               | N/A                                                              |
| `enabled`                                                        | *boolean*                                                        | :heavy_minus_sign:                                               | N/A                                                              |
| `secret`                                                         | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
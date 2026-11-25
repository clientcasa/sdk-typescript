# ListWebhooksRequest

## Example Usage

```typescript
import { ListWebhooksRequest } from "@clientcasa/sdk/models/operations";

let value: ListWebhooksRequest = {};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `page`                                                                           | *number*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |
| `pageSize`                                                                       | *number*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |
| `enabled`                                                                        | [operations.Enabled](../../models/operations/enabled.md)                         | :heavy_minus_sign:                                                               | Literal `true` or `false`. Any other value is rejected with 400 invalid_request. |
| `event`                                                                          | [operations.ListWebhooksEvent](../../models/operations/list-webhooks-event.md)   | :heavy_minus_sign:                                                               | N/A                                                                              |
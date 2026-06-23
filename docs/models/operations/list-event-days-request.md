# ListEventDaysRequest

## Example Usage

```typescript
import { ListEventDaysRequest } from "@clientcasa/sdk/models/operations";

let value: ListEventDaysRequest = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         | Example                                                                             |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `page`                                                                              | *number*                                                                            | :heavy_minus_sign:                                                                  | N/A                                                                                 |                                                                                     |
| `pageSize`                                                                          | *number*                                                                            | :heavy_minus_sign:                                                                  | N/A                                                                                 |                                                                                     |
| `status`                                                                            | [operations.ListEventDaysStatus](../../models/operations/list-event-days-status.md) | :heavy_minus_sign:                                                                  | N/A                                                                                 |                                                                                     |
| `projectId`                                                                         | *string*                                                                            | :heavy_minus_sign:                                                                  | UUID v4                                                                             | 550e8400-e29b-41d4-a716-446655440000                                                |
| `clientId`                                                                          | *string*                                                                            | :heavy_minus_sign:                                                                  | UUID v4                                                                             | 550e8400-e29b-41d4-a716-446655440000                                                |
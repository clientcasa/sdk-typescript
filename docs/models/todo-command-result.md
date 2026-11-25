# TodoCommandResult

## Example Usage

```typescript
import { TodoCommandResult } from "@clientcasa/sdk/models";

let value: TodoCommandResult = {
  todoId: "550e8400-e29b-41d4-a716-446655440000",
  eventId: "550e8400-e29b-41d4-a716-446655440000",
  revision: 101620,
  status: "<value>",
  billing: "preparing",
};
```

## Fields

| Field                                  | Type                                   | Required                               | Description                            | Example                                |
| -------------------------------------- | -------------------------------------- | -------------------------------------- | -------------------------------------- | -------------------------------------- |
| `todoId`                               | *string*                               | :heavy_check_mark:                     | UUID v4                                | 550e8400-e29b-41d4-a716-446655440000   |
| `eventId`                              | *string*                               | :heavy_check_mark:                     | UUID v4                                | 550e8400-e29b-41d4-a716-446655440000   |
| `revision`                             | *number*                               | :heavy_check_mark:                     | N/A                                    |                                        |
| `status`                               | *string*                               | :heavy_check_mark:                     | N/A                                    |                                        |
| `billing`                              | [models.Billing](../models/billing.md) | :heavy_check_mark:                     | N/A                                    |                                        |
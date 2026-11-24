# ListTodosRequest

## Example Usage

```typescript
import { ListTodosRequest } from "@clientcasa/sdk/models/operations";

let value: ListTodosRequest = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  eventDayId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                | Example                                                                    |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `projectId`                                                                | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `clientId`                                                                 | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `scope`                                                                    | [operations.ListTodosScope](../../models/operations/list-todos-scope.md)   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `eventDayId`                                                               | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `mode`                                                                     | [operations.ListTodosMode](../../models/operations/list-todos-mode.md)     | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `start`                                                                    | [Date](../../types/rfcdate.md)                                             | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `end`                                                                      | [Date](../../types/rfcdate.md)                                             | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `after`                                                                    | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `limit`                                                                    | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `kind`                                                                     | [operations.ListTodosKind](../../models/operations/list-todos-kind.md)     | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `status`                                                                   | [operations.ListTodosStatus](../../models/operations/list-todos-status.md) | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
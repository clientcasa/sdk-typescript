# TodoUpdate

## Example Usage

```typescript
import { TodoUpdate } from "@clientcasa/sdk/models";

let value: TodoUpdate = {
  commandId: "550e8400-e29b-41d4-a716-446655440000",
  expectedRevision: 120483,
  fields: {},
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                | Example                                                    |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `commandId`                                                | *string*                                                   | :heavy_check_mark:                                         | UUID v4                                                    | 550e8400-e29b-41d4-a716-446655440000                       |
| `expectedRevision`                                         | *number*                                                   | :heavy_check_mark:                                         | N/A                                                        |                                                            |
| `fields`                                                   | [models.TodoUpdateFields](../models/todo-update-fields.md) | :heavy_check_mark:                                         | N/A                                                        |                                                            |
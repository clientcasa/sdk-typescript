# TodoCreate

## Example Usage

```typescript
import { TodoCreate } from "@clientcasa/sdk/models";

let value: TodoCreate = {
  intent: "create",
  commandId: "b585d732-1e61-4545-bc63-c17a0bc1937b",
  todoId: "eb1b8485-8fbd-4bb9-858d-b8e035f9e592",
  businessId: "aa66b2f2-a223-4d99-9f06-a19bf66cec0f",
  title: "<value>",
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `intent`                                                   | [models.Intent](../models/intent.md)                       | :heavy_check_mark:                                         | N/A                                                        |
| `commandId`                                                | *string*                                                   | :heavy_check_mark:                                         | N/A                                                        |
| `todoId`                                                   | *string*                                                   | :heavy_check_mark:                                         | N/A                                                        |
| `businessId`                                               | *string*                                                   | :heavy_check_mark:                                         | N/A                                                        |
| `projectId`                                                | *string*                                                   | :heavy_minus_sign:                                         | N/A                                                        |
| `clientId`                                                 | *string*                                                   | :heavy_minus_sign:                                         | N/A                                                        |
| `title`                                                    | *string*                                                   | :heavy_check_mark:                                         | N/A                                                        |
| `fields`                                                   | [models.TodoCreateFields](../models/todo-create-fields.md) | :heavy_minus_sign:                                         | N/A                                                        |
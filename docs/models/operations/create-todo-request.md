# CreateTodoRequest

## Example Usage

```typescript
import { CreateTodoRequest } from "@clientcasa/sdk/models/operations";

let value: CreateTodoRequest = {
  idempotencyKey: "create-client-2026-05-24-a1b2c3",
  body: {
    intent: "create",
    commandId: "d66a8412-2b63-496a-876f-611fefb2b04c",
    todoId: "0aaf1eaf-685d-4644-957e-fd8f88ca23e2",
    businessId: "0dc36033-eade-4896-baa9-284d0c4c72cb",
    title: "<value>",
  },
};
```

## Fields

| Field                                                                                                                                                                                                        | Type                                                                                                                                                                                                         | Required                                                                                                                                                                                                     | Description                                                                                                                                                                                                  | Example                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `idempotencyKey`                                                                                                                                                                                             | *string*                                                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                           | Optional unique key that makes this request safely retryable. Replaying the same key returns the original response instead of creating a duplicate; reusing a key with a different request body returns 409. | create-client-2026-05-24-a1b2c3                                                                                                                                                                              |
| `body`                                                                                                                                                                                                       | [models.TodoCreate](../../models/todo-create.md)                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                                                           | N/A                                                                                                                                                                                                          |                                                                                                                                                                                                              |
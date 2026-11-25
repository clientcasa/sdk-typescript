# TodoList

## Example Usage

```typescript
import { TodoList } from "@clientcasa/sdk/models";

let value: TodoList = {
  data: [],
  items: [
    {
      "key": "<value>",
    },
  ],
  complete: true,
  pagination: {
    nextCursor: "<value>",
  },
  coverage: {
    after: "<value>",
    next: "<value>",
    stopped: false,
  },
  sources: {
    "key": "<value>",
    "key1": "<value>",
  },
  evaluatedAt: new Date("2024-01-27T22:15:15.247Z"),
  revisions: {
    "key": 7386.56,
    "key1": 5494.34,
    "key2": 6350.57,
  },
  nextAction: {},
  notice: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `data`                                                                                        | [models.Todo](../models/todo.md)[]                                                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `items`                                                                                       | Record<string, *any*>[]                                                                       | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `complete`                                                                                    | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `pagination`                                                                                  | [models.TodoListPagination](../models/todo-list-pagination.md)                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `coverage`                                                                                    | [models.TodoListCoverage](../models/todo-list-coverage.md)                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `sources`                                                                                     | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `evaluatedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |
| `revisions`                                                                                   | Record<string, *number*>                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `nextAction`                                                                                  | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `notice`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
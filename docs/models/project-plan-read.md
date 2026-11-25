# ProjectPlanRead

## Example Usage

```typescript
import { ProjectPlanRead } from "@clientcasa/sdk/models";

let value: ProjectPlanRead = {
  data: [],
  items: [
    {
      "key": "<value>",
      "key1": "<value>",
      "key2": "<value>",
    },
    {
      "key": "<value>",
      "key1": "<value>",
      "key2": "<value>",
    },
    {},
  ],
  complete: false,
  pagination: {
    nextCursor: "<value>",
  },
  coverage: {
    after: "<value>",
    next: "<value>",
    stopped: true,
  },
  sources: {
    "key": "<value>",
  },
  evaluatedAt: new Date("2026-06-29T02:38:03.364Z"),
  revisions: {
    "key": 5100.35,
  },
  nextAction: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  notice: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `data`                                                                                        | [models.Todo](../models/todo.md)[]                                                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `items`                                                                                       | Record<string, *any*>[]                                                                       | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `complete`                                                                                    | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `pagination`                                                                                  | [models.ProjectPlanReadPagination](../models/project-plan-read-pagination.md)                 | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `coverage`                                                                                    | [models.ProjectPlanReadCoverage](../models/project-plan-read-coverage.md)                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `sources`                                                                                     | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `evaluatedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |
| `revisions`                                                                                   | Record<string, *number*>                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `nextAction`                                                                                  | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `notice`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
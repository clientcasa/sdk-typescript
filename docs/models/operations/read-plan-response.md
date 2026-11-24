# ReadPlanResponse

## Example Usage

```typescript
import { ReadPlanResponse } from "@clientcasa/sdk/models/operations";

let value: ReadPlanResponse = {
  result: {
    data: [],
    items: [],
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
      "key1": "<value>",
      "key2": "<value>",
    },
    evaluatedAt: new Date("2025-10-20T11:00:38.809Z"),
    revisions: {
      "key": 4220.23,
    },
    nextAction: {
      "key": "<value>",
      "key1": "<value>",
    },
    notice: "<value>",
  },
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `result`                                                    | [models.ProjectPlanRead](../../models/project-plan-read.md) | :heavy_check_mark:                                          | N/A                                                         |
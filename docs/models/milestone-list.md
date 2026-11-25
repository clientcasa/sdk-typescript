# MilestoneList

## Example Usage

```typescript
import { MilestoneList } from "@clientcasa/sdk/models";

let value: MilestoneList = {
  data: [],
  pagination: {
    page: 516578,
    pageSize: 475915,
    total: 168292,
    totalPages: 953541,
    hasMore: true,
    nextCursor: "<value>",
  },
  complete: false,
  coverage: {
    after: "<value>",
    next: "<value>",
    stopped: true,
  },
  sources: {
    todos: {
      complete: true,
      stopped: true,
      unavailable: false,
    },
  },
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `data`                                                                       | [models.Milestone](../models/milestone.md)[]                                 | :heavy_check_mark:                                                           | N/A                                                                          |
| `pagination`                                                                 | [models.MilestoneCursorPagination](../models/milestone-cursor-pagination.md) | :heavy_check_mark:                                                           | N/A                                                                          |
| `complete`                                                                   | *boolean*                                                                    | :heavy_check_mark:                                                           | N/A                                                                          |
| `coverage`                                                                   | [models.MilestoneListCoverage](../models/milestone-list-coverage.md)         | :heavy_check_mark:                                                           | N/A                                                                          |
| `sources`                                                                    | [models.Sources](../models/sources.md)                                       | :heavy_check_mark:                                                           | N/A                                                                          |
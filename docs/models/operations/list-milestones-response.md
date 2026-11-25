# ListMilestonesResponse

## Example Usage

```typescript
import { ListMilestonesResponse } from "@clientcasa/sdk/models/operations";

let value: ListMilestonesResponse = {
  result: {
    data: [
      {
        id: "550e8400-e29b-41d4-a716-446655440000",
        parentType: "client-documents",
        parentId: "550e8400-e29b-41d4-a716-446655440000",
        title: "<value>",
        description:
          "modulo dearly around although ferociously infatuated affiliate furiously shabby",
        date: new Date("2024-08-22"),
        time: "<value>",
        status: "in-progress",
        completedAt: null,
        assigneeId: "550e8400-e29b-41d4-a716-446655440000",
        catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
        sortOrder: 119795,
        createdAt: new Date("2026-12-30T07:17:10.681Z"),
        updatedAt: new Date("2025-01-24T21:35:27.673Z"),
      },
    ],
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
  },
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `result`                                               | [models.MilestoneList](../../models/milestone-list.md) | :heavy_check_mark:                                     | N/A                                                    |
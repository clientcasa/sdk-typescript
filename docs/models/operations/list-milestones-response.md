# ListMilestonesResponse

OK

## Example Usage

```typescript
import { ListMilestonesResponse } from "@clientcasa/sdk/models/operations";

let value: ListMilestonesResponse = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      parentType: "projects",
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
    page: 299018,
    pageSize: 331897,
    total: 615983,
    totalPages: 226919,
    hasMore: true,
  },
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `data`                                                   | [models.Milestone](../../models/milestone.md)[]          | :heavy_check_mark:                                       | N/A                                                      |
| `pagination`                                             | [models.PaginationMeta](../../models/pagination-meta.md) | :heavy_check_mark:                                       | N/A                                                      |
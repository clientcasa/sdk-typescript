# ListTimelineItemsResponse

## Example Usage

```typescript
import { ListTimelineItemsResponse } from "@clientcasa/sdk/models/operations";

let value: ListTimelineItemsResponse = {
  result: {
    data: [
      {
        id: "550e8400-e29b-41d4-a716-446655440000",
        eventDayId: "<id>",
        title: "<value>",
        description:
          "restfully why spear where out amazing wealthy tidy cooperative",
        categoryId: "<id>",
        sortOrder: 2311.43,
        trackId: "<id>",
        requestedStartTime: null,
        durationMinutes: 78.2,
        bufferBeforeMinutes: 4048.36,
        bufferAfterMinutes: null,
        travelTimeMinutes: 9831.54,
        locked: true,
        anchorType: "fixed",
        anchorKey: "<value>",
        location: "<value>",
        visibleTo: [
          "venue",
        ],
        vendorIds: [],
        status: "in-progress",
        createdAt: new Date("2025-01-13T15:36:31.237Z"),
        updatedAt: new Date("2024-10-11T14:07:08.662Z"),
      },
    ],
    pagination: {
      page: 299018,
      pageSize: 331897,
      total: 615983,
      totalPages: 226919,
      hasMore: true,
    },
  },
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `result`                                                      | [models.TimelineItemList](../../models/timeline-item-list.md) | :heavy_check_mark:                                            | N/A                                                           |
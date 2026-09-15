# ListTimelineItemsResponse

## Example Usage

```typescript
import { ListTimelineItemsResponse } from "@clientcasa/sdk/models/operations";

let value: ListTimelineItemsResponse = {
  result: {
    data: [
      {
        id: "550e8400-e29b-41d4-a716-446655440000",
        eventDayId: "550e8400-e29b-41d4-a716-446655440000",
        title: "<value>",
        description:
          "restfully why spear where out amazing wealthy tidy cooperative",
        categoryId: "550e8400-e29b-41d4-a716-446655440000",
        sortOrder: 7604.38,
        trackId: "<id>",
        requestedStartTime: "<value>",
        durationMinutes: 750.73,
        bufferBeforeMinutes: null,
        bufferAfterMinutes: 4048.36,
        travelTimeMinutes: null,
        locked: false,
        anchorType: "custom-event",
        anchorKey: "<value>",
        location: "<value>",
        visibleTo: [],
        vendorIds: [
          "550e8400-e29b-41d4-a716-446655440000",
        ],
        status: "skipped",
        createdAt: new Date("2026-04-13T01:55:12.896Z"),
        updatedAt: new Date("2025-08-01T05:47:17.016Z"),
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
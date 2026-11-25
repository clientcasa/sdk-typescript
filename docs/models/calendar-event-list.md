# CalendarEventList

## Example Usage

```typescript
import { CalendarEventList } from "@clientcasa/sdk/models";

let value: CalendarEventList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      title: "<value>",
      description: "through um oof whether",
      location: "<value>",
      startDateTime: new Date("2026-03-17T18:35:38.195Z"),
      endDateTime: new Date("2024-11-01T23:05:11.696Z"),
      allDay: true,
      projectId: "550e8400-e29b-41d4-a716-446655440000",
      clientId: "550e8400-e29b-41d4-a716-446655440000",
      actionable: false,
      completedAt: new Date("2025-10-09T16:04:08.708Z"),
      recurring: false,
      rrule: null,
      recurrenceEnd: new Date("2025-12-01T16:05:12.783Z"),
      source: "microsoft",
      readOnly: false,
      createdAt: new Date("2026-07-22T12:56:44.895Z"),
      updatedAt: new Date("2025-04-12T12:21:31.328Z"),
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

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `data`                                                | [models.CalendarEvent](../models/calendar-event.md)[] | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
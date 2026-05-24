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
      startDateTime: new Date("2025-12-13T19:51:20.875Z"),
      endDateTime: new Date("2026-03-17T18:35:38.195Z"),
      allDay: true,
      projectId: "550e8400-e29b-41d4-a716-446655440000",
      clientId: "550e8400-e29b-41d4-a716-446655440000",
      actionable: true,
      completedAt: new Date("2026-04-05T07:41:52.207Z"),
      recurring: false,
      rrule: "<value>",
      recurrenceEnd: null,
      source: "manual",
      readOnly: false,
      createdAt: new Date("2025-10-17T01:12:52.101Z"),
      updatedAt: new Date("2026-07-06T05:06:14.054Z"),
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
# ListCalendarEventsResponse

## Example Usage

```typescript
import { ListCalendarEventsResponse } from "@clientcasa/sdk/models/operations";

let value: ListCalendarEventsResponse = {
  result: {
    data: [],
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

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `result`                                                        | [models.CalendarEventList](../../models/calendar-event-list.md) | :heavy_check_mark:                                              | N/A                                                             |
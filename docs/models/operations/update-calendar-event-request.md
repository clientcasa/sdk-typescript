# UpdateCalendarEventRequest

## Example Usage

```typescript
import { UpdateCalendarEventRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateCalendarEventRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    projectId: "550e8400-e29b-41d4-a716-446655440000",
    clientId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `id`                                                                | *string*                                                            | :heavy_check_mark:                                                  | UUID v4                                                             | 550e8400-e29b-41d4-a716-446655440000                                |
| `body`                                                              | [models.CalendarEventUpdate](../../models/calendar-event-update.md) | :heavy_check_mark:                                                  | N/A                                                                 |                                                                     |
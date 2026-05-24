# CreateCalendarEventRequest

## Example Usage

```typescript
import { CreateCalendarEventRequest } from "@clientcasa/sdk/models/operations";

let value: CreateCalendarEventRequest = {
  idempotencyKey: "create-client-2026-05-24-a1b2c3",
  body: {
    title: "<value>",
    startDateTime: new Date("2025-07-20T19:51:13.952Z"),
    endDateTime: new Date("2026-12-08T05:49:05.458Z"),
    projectId: "550e8400-e29b-41d4-a716-446655440000",
    clientId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                                                                                                                                                                       | Type                                                                                                                                                                                                        | Required                                                                                                                                                                                                    | Description                                                                                                                                                                                                 | Example                                                                                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                                                                                                                            | *string*                                                                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                                                                          | Optional unique key that makes this create safely retryable. Replaying the same key returns the original response instead of creating a duplicate; reusing a key with a different request body returns 409. | create-client-2026-05-24-a1b2c3                                                                                                                                                                             |
| `body`                                                                                                                                                                                                      | [models.CalendarEventCreate](../../models/calendar-event-create.md)                                                                                                                                         | :heavy_check_mark:                                                                                                                                                                                          | N/A                                                                                                                                                                                                         |                                                                                                                                                                                                             |
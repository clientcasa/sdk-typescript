# EventDay

## Example Usage

```typescript
import { EventDay } from "@clientcasa/sdk/models";

let value: EventDay = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  name: null,
  date: new Date("2024-06-20"),
  status: "published",
  ceremonyTime: "<value>",
  eventStartTime: "<value>",
  venueTimezone: "<value>",
  venueAddress: {
    name: null,
    street: "Mante Highway",
    city: "Joanaboro",
    state: null,
    zip: "09600-9225",
    country: "Bonaire, Sint Eustatius and Saba",
    lat: 3434.52,
    lng: 426.73,
  },
  venueNotes: "<value>",
  dayStartMinute: 909846,
  dayEndMinute: 405788,
  customAnchors: [
    {
      key: "<key>",
      label: null,
      time: "<value>",
    },
  ],
  isPrimary: false,
  sortOrder: 362129,
  createdAt: new Date("2025-07-31T03:01:45.873Z"),
  updatedAt: new Date("2026-08-27T13:51:33.750Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `projectId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `clientId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `date`                                                                                        | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | [models.EventDayStatus](../models/event-day-status.md)                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `ceremonyTime`                                                                                | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `eventStartTime`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `venueTimezone`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `venueAddress`                                                                                | [models.VenueAddress](../models/venue-address.md)                                             | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `venueNotes`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `dayStartMinute`                                                                              | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `dayEndMinute`                                                                                | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `customAnchors`                                                                               | [models.EventDayCustomAnchor](../models/event-day-custom-anchor.md)[]                         | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `isPrimary`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `sortOrder`                                                                                   | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
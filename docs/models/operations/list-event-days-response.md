# ListEventDaysResponse

## Example Usage

```typescript
import { ListEventDaysResponse } from "@clientcasa/sdk/models/operations";

let value: ListEventDaysResponse = {
  result: {
    data: [
      {
        id: "550e8400-e29b-41d4-a716-446655440000",
        projectId: "550e8400-e29b-41d4-a716-446655440000",
        clientId: "550e8400-e29b-41d4-a716-446655440000",
        name: "<value>",
        date: new Date("2025-06-04"),
        status: "archived",
        ceremonyTime: null,
        eventStartTime: "<value>",
        venueTimezone: "<value>",
        venueAddress: {
          name: null,
          street: "Mante Highway",
          city: "Joanaboro",
          state: null,
          zip: "09600-9225",
          country: "Bonaire, Sint Eustatius and Saba",
        },
        venueNotes: "<value>",
        dayStartMinute: 945347,
        dayEndMinute: null,
        customAnchors: [],
        isPrimary: true,
        sortOrder: 809019,
        createdAt: new Date("2024-10-05T18:58:03.296Z"),
        updatedAt: new Date("2025-11-14T11:20:09.502Z"),
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

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `result`                                              | [models.EventDayList](../../models/event-day-list.md) | :heavy_check_mark:                                    | N/A                                                   |
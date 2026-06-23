# EventDayVendorList

## Example Usage

```typescript
import { EventDayVendorList } from "@clientcasa/sdk/models";

let value: EventDayVendorList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      eventDayId: "<id>",
      vendorId: "<id>",
      role: null,
      callTime: "<value>",
      coverageStartTime: "<value>",
      coverageEndTime: "<value>",
      mealProvided: false,
      mealNotes: "<value>",
      pointOfContact: "<value>",
      pointOfContactPhone: "<value>",
      internalNotes: "<value>",
      confirmationStatus: "declined",
      createdAt: new Date("2025-10-22T11:00:01.721Z"),
      updatedAt: new Date("2026-11-24T03:50:05.946Z"),
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
| `data`                                                   | [models.EventDayVendor](../models/event-day-vendor.md)[] | :heavy_check_mark:                                       | N/A                                                      |
| `pagination`                                             | [models.PaginationMeta](../models/pagination-meta.md)    | :heavy_check_mark:                                       | N/A                                                      |
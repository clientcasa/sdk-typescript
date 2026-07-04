# VenueList

## Example Usage

```typescript
import { VenueList } from "@clientcasa/sdk/models";

let value: VenueList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      name: "<value>",
      website: "<value>",
      address: {
        line1: "<value>",
        line2: "<value>",
        city: "Perris",
        state: "North Dakota",
        postalCode: "26047-5508",
        country: "Egypt",
      },
      timezone: "Asia/Shanghai",
      contacts: [],
      spaces: [
        {
          name: "<value>",
          notes: "<value>",
        },
      ],
      notes: "<value>",
      tagIds: [
        "550e8400-e29b-41d4-a716-446655440000",
      ],
      status: "active",
      createdAt: new Date("2026-02-22T08:22:25.640Z"),
      updatedAt: new Date("2025-11-24T19:47:40.533Z"),
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
| `data`                                                | [models.Venue](../models/venue.md)[]                  | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
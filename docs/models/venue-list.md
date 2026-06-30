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
        lat: 6514.29,
        lng: 7719.82,
      },
      timezone: "Pacific/Majuro",
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
      status: "archived",
      createdAt: new Date("2026-08-19T01:44:18.186Z"),
      updatedAt: new Date("2024-02-18T05:15:26.571Z"),
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
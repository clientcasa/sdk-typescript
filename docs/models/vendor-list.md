# VendorList

## Example Usage

```typescript
import { VendorList } from "@clientcasa/sdk/models";

let value: VendorList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      name: "<value>",
      companyName: "Bailey - Kessler",
      categoryId: "550e8400-e29b-41d4-a716-446655440000",
      email: "Maye1@gmail.com",
      phone: "(376) 350-1734",
      website: "<value>",
      address: {
        street: "O'Keefe Fields",
        city: "Warner Robins",
        state: "Indiana",
        zip: "34134",
      },
      notes: "<value>",
      rating: "neutral",
      defaultSetupMinutes: 9244.47,
      defaultTeardownMinutes: 976.91,
      linkedContactId: "550e8400-e29b-41d4-a716-446655440000",
      status: "archived",
      createdAt: new Date("2024-12-13T10:59:41.554Z"),
      updatedAt: new Date("2025-04-25T04:07:47.005Z"),
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
| `data`                                                | [models.Vendor](../models/vendor.md)[]                | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
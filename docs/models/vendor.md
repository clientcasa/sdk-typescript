# Vendor

## Example Usage

```typescript
import { Vendor } from "@clientcasa/sdk/models";

let value: Vendor = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  companyName: "Hilll, Miller and Cassin",
  categoryId: "550e8400-e29b-41d4-a716-446655440000",
  email: "Juston.Hirthe-Kutch91@hotmail.com",
  phone: null,
  website: "<value>",
  address: {
    street: "O'Keefe Fields",
    city: "Warner Robins",
    state: "Indiana",
    zip: "34134",
  },
  notes: "<value>",
  rating: null,
  defaultSetupMinutes: 6432.52,
  defaultTeardownMinutes: 4842.05,
  linkedContactId: "550e8400-e29b-41d4-a716-446655440000",
  status: "archived",
  createdAt: new Date("2026-11-17T09:35:41.892Z"),
  updatedAt: new Date("2026-03-16T21:20:10.749Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `companyName`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `categoryId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `email`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `phone`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `website`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `address`                                                                                     | [models.VendorAddress](../models/vendor-address.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `notes`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `rating`                                                                                      | [models.VendorRating](../models/vendor-rating.md)                                             | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `defaultSetupMinutes`                                                                         | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `defaultTeardownMinutes`                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `linkedContactId`                                                                             | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `status`                                                                                      | [models.VendorStatus](../models/vendor-status.md)                                             | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
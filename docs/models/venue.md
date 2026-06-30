# Venue

## Example Usage

```typescript
import { Venue } from "@clientcasa/sdk/models";

let value: Venue = {
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
  timezone: "Europe/Berlin",
  contacts: [
    {
      name: "<value>",
      role: "<value>",
      email: "Frankie38@gmail.com",
      phone: null,
    },
  ],
  spaces: [],
  notes: "<value>",
  tagIds: [
    "550e8400-e29b-41d4-a716-446655440000",
  ],
  status: "archived",
  createdAt: new Date("2024-06-11T21:29:24.884Z"),
  updatedAt: new Date("2024-03-13T22:51:21.942Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `website`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `address`                                                                                     | [models.VenueAddress1](../models/venue-address1.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `timezone`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `contacts`                                                                                    | [models.VenueContact](../models/venue-contact.md)[]                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `spaces`                                                                                      | [models.VenueSpace](../models/venue-space.md)[]                                               | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `notes`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `tagIds`                                                                                      | *string*[]                                                                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | [models.VenueStatus](../models/venue-status.md)                                               | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
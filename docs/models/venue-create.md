# VenueCreate

## Example Usage

```typescript
import { VenueCreate } from "@clientcasa/sdk/models";

let value: VenueCreate = {
  name: "<value>",
  tagIds: [
    "550e8400-e29b-41d4-a716-446655440000",
  ],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `website`                                                        | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `address`                                                        | [models.VenueCreateAddress](../models/venue-create-address.md)   | :heavy_minus_sign:                                               | N/A                                                              |
| `timezone`                                                       | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `contacts`                                                       | [models.VenueCreateContact](../models/venue-create-contact.md)[] | :heavy_minus_sign:                                               | N/A                                                              |
| `spaces`                                                         | [models.VenueCreateSpace](../models/venue-create-space.md)[]     | :heavy_minus_sign:                                               | N/A                                                              |
| `notes`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `tagIds`                                                         | *string*[]                                                       | :heavy_minus_sign:                                               | N/A                                                              |
| `status`                                                         | [models.VenueCreateStatus](../models/venue-create-status.md)     | :heavy_minus_sign:                                               | N/A                                                              |
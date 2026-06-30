# VenueUpdate

## Example Usage

```typescript
import { VenueUpdate } from "@clientcasa/sdk/models";

let value: VenueUpdate = {
  tagIds: [
    "550e8400-e29b-41d4-a716-446655440000",
  ],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `website`                                                        | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `address`                                                        | [models.VenueUpdateAddress](../models/venue-update-address.md)   | :heavy_minus_sign:                                               | N/A                                                              |
| `timezone`                                                       | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `contacts`                                                       | [models.VenueUpdateContact](../models/venue-update-contact.md)[] | :heavy_minus_sign:                                               | N/A                                                              |
| `spaces`                                                         | [models.VenueUpdateSpace](../models/venue-update-space.md)[]     | :heavy_minus_sign:                                               | N/A                                                              |
| `notes`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `tagIds`                                                         | *string*[]                                                       | :heavy_minus_sign:                                               | N/A                                                              |
| `status`                                                         | [models.VenueUpdateStatus](../models/venue-update-status.md)     | :heavy_minus_sign:                                               | N/A                                                              |
# UpdateVenueRequest

## Example Usage

```typescript
import { UpdateVenueRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateVenueRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    tagIds: [
      "550e8400-e29b-41d4-a716-446655440000",
    ],
  },
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        | Example                                            |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `id`                                               | *string*                                           | :heavy_check_mark:                                 | UUID v4                                            | 550e8400-e29b-41d4-a716-446655440000               |
| `body`                                             | [models.VenueUpdate](../../models/venue-update.md) | :heavy_check_mark:                                 | N/A                                                |                                                    |
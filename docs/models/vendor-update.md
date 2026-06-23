# VendorUpdate

## Example Usage

```typescript
import { VendorUpdate } from "@clientcasa/sdk/models";

let value: VendorUpdate = {
  categoryId: "550e8400-e29b-41d4-a716-446655440000",
  linkedContactId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `companyName`                                                    | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `categoryId`                                                     | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `email`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `phone`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `website`                                                        | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `address`                                                        | [models.VendorUpdateAddress](../models/vendor-update-address.md) | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `notes`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `rating`                                                         | [models.VendorUpdateRating](../models/vendor-update-rating.md)   | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `defaultSetupMinutes`                                            | *number*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `defaultTeardownMinutes`                                         | *number*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `linkedContactId`                                                | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `status`                                                         | [models.VendorUpdateStatus](../models/vendor-update-status.md)   | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
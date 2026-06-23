# UpdateVendorRequest

## Example Usage

```typescript
import { UpdateVendorRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateVendorRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    categoryId: "550e8400-e29b-41d4-a716-446655440000",
    linkedContactId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          | Example                                              |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `id`                                                 | *string*                                             | :heavy_check_mark:                                   | UUID v4                                              | 550e8400-e29b-41d4-a716-446655440000                 |
| `body`                                               | [models.VendorUpdate](../../models/vendor-update.md) | :heavy_check_mark:                                   | N/A                                                  |                                                      |
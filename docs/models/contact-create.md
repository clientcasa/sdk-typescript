# ContactCreate

## Example Usage

```typescript
import { ContactCreate } from "@clientcasa/sdk/models";

let value: ContactCreate = {
  name: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  | Example                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `name`                                                       | *string*                                                     | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `email`                                                      | *string*                                                     | :heavy_minus_sign:                                           | N/A                                                          |                                                              |
| `phone`                                                      | *string*                                                     | :heavy_minus_sign:                                           | N/A                                                          |                                                              |
| `title`                                                      | *string*                                                     | :heavy_minus_sign:                                           | N/A                                                          |                                                              |
| `role`                                                       | [models.ContactCreateRole](../models/contact-create-role.md) | :heavy_minus_sign:                                           | N/A                                                          |                                                              |
| `isPrimary`                                                  | *boolean*                                                    | :heavy_minus_sign:                                           | N/A                                                          |                                                              |
| `clientId`                                                   | *string*                                                     | :heavy_minus_sign:                                           | UUID v4                                                      | 550e8400-e29b-41d4-a716-446655440000                         |
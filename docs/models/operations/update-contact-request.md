# UpdateContactRequest

## Example Usage

```typescript
import { UpdateContactRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateContactRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    clientId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            | Example                                                |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `id`                                                   | *string*                                               | :heavy_check_mark:                                     | UUID v4                                                | 550e8400-e29b-41d4-a716-446655440000                   |
| `body`                                                 | [models.ContactUpdate](../../models/contact-update.md) | :heavy_check_mark:                                     | N/A                                                    |                                                        |
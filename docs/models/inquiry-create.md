# InquiryCreate

## Example Usage

```typescript
import { InquiryCreate } from "@clientcasa/sdk/models";

let value: InquiryCreate = {
  name: "<value>",
  email: "Sigrid61@hotmail.com",
  contactId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
| `email`                                                          | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
| `phone`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `preferredDate`                                                  | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `message`                                                        | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `source`                                                         | [models.InquiryCreateSource](../models/inquiry-create-source.md) | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `customAnswers`                                                  | Record<string, *any*>                                            | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `contactId`                                                      | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `notes`                                                          | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
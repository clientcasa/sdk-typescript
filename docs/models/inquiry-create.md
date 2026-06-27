# InquiryCreate

## Example Usage

```typescript
import { InquiryCreate } from "@clientcasa/sdk/models";

let value: InquiryCreate = {
  name: "Jane Doe",
  email: "jane@example.com",
  preferredDate: "2026-09-12",
  fields: {
    "Event Type": "Wedding",
    "Venue": "The Grand Hall",
  },
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            | Example                                                |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `name`                                                 | *string*                                               | :heavy_check_mark:                                     | N/A                                                    | Jane Doe                                               |
| `email`                                                | *string*                                               | :heavy_check_mark:                                     | N/A                                                    | jane@example.com                                       |
| `phone`                                                | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |                                                        |
| `preferredDate`                                        | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    | 2026-09-12                                             |
| `message`                                              | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |                                                        |
| `fields`                                               | Record<string, *models.Fields*>                        | :heavy_minus_sign:                                     | N/A                                                    | {<br/>"Event Type": "Wedding",<br/>"Venue": "The Grand Hall"<br/>} |
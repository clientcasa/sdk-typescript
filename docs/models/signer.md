# Signer

## Example Usage

```typescript
import { Signer } from "@clientcasa/sdk/models";

let value: Signer = {
  contactId: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  email: "Felix_McGlynn@hotmail.com",
  role: "<value>",
  order: 541624,
  status: "<value>",
  signedAt: new Date("2024-04-03T10:44:21.275Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `contactId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `email`                                                                                       | *models.Email*                                                                                | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `role`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `order`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `signedAt`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
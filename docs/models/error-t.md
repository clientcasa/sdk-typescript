# ErrorT

## Example Usage

```typescript
import { ErrorT } from "@clientcasa/sdk/models";

let value: ErrorT = {
  code: "unauthorized",
  message: "<value>",
  requestId: "<id>",
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `code`                           | [models.Code](../models/code.md) | :heavy_check_mark:               | N/A                              |
| `message`                        | *string*                         | :heavy_check_mark:               | N/A                              |
| `requestId`                      | *string*                         | :heavy_check_mark:               | N/A                              |
| `details`                        | Record<string, *any*>            | :heavy_minus_sign:               | N/A                              |
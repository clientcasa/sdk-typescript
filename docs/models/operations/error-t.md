# ErrorT

## Example Usage

```typescript
import { ErrorT } from "@clientcasa/sdk/models/operations";

let value: ErrorT = {
  code: "conflict",
  message: "<value>",
  requestId: "<id>",
  details: {
    code: "transaction_delete_preview_required",
    preview: {
      ids: [
        "550e8400-e29b-41d4-a716-446655440000",
      ],
      impacts: [],
    },
    acknowledgement: "<value>",
  },
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `code`                                                   | [operations.Code](../../models/operations/code.md)       | :heavy_check_mark:                                       | N/A                                                      |
| `message`                                                | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `requestId`                                              | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `details`                                                | [operations.Details](../../models/operations/details.md) | :heavy_check_mark:                                       | N/A                                                      |
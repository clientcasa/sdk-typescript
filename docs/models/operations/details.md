# Details

## Example Usage

```typescript
import { Details } from "@clientcasa/sdk/models/operations";

let value: Details = {
  code: "transaction_delete_preview_required",
  preview: {
    ids: [
      "550e8400-e29b-41d4-a716-446655440000",
    ],
    impacts: [],
  },
  acknowledgement: "<value>",
};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                                 | [operations.CodeTransactionDeletePreviewRequired](../../models/operations/code-transaction-delete-preview-required.md) | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `preview`                                                                                                              | [operations.Preview](../../models/operations/preview.md)                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `acknowledgement`                                                                                                      | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
# DeleteTransactionRequest

## Example Usage

```typescript
import { DeleteTransactionRequest } from "@clientcasa/sdk/models/operations";

let value: DeleteTransactionRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            | Example                                                                |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `id`                                                                   | *string*                                                               | :heavy_check_mark:                                                     | UUID v4                                                                | 550e8400-e29b-41d4-a716-446655440000                                   |
| `xTransactionDeleteAcknowledgement`                                    | *string*                                                               | :heavy_minus_sign:                                                     | The acknowledgement returned with transaction_delete_preview_required. |                                                                        |
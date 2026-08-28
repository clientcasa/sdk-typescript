# ClientCreate

## Example Usage

```typescript
import { ClientCreate } from "@clientcasa/sdk/models";

let value: ClientCreate = {
  name: "<value>",
  businessId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    | Example                                                        |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `name`                                                         | *string*                                                       | :heavy_check_mark:                                             | N/A                                                            |                                                                |
| `status`                                                       | [models.ClientCreateStatus](../models/client-create-status.md) | :heavy_minus_sign:                                             | N/A                                                            |                                                                |
| `businessId`                                                   | *string*                                                       | :heavy_minus_sign:                                             | UUID v4                                                        | 550e8400-e29b-41d4-a716-446655440000                           |
| `notes`                                                        | *string*                                                       | :heavy_minus_sign:                                             | N/A                                                            |                                                                |
| `taxSettings`                                                  | [models.ClientTaxSettings](../models/client-tax-settings.md)   | :heavy_minus_sign:                                             | N/A                                                            |                                                                |
| `invoiceRemindersEnabled`                                      | *boolean*                                                      | :heavy_minus_sign:                                             | N/A                                                            |                                                                |
| `attachInvoicePdf`                                             | *boolean*                                                      | :heavy_minus_sign:                                             | N/A                                                            |                                                                |
| `attachReceiptPdf`                                             | *boolean*                                                      | :heavy_minus_sign:                                             | N/A                                                            |                                                                |
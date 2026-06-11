# ClientCreate

## Example Usage

```typescript
import { ClientCreate } from "@clientcasa/sdk/models";

let value: ClientCreate = {
  name: "<value>",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `name`                                                         | *string*                                                       | :heavy_check_mark:                                             | N/A                                                            |
| `status`                                                       | [models.ClientCreateStatus](../models/client-create-status.md) | :heavy_minus_sign:                                             | N/A                                                            |
| `notes`                                                        | *string*                                                       | :heavy_minus_sign:                                             | N/A                                                            |
| `taxSettings`                                                  | [models.ClientTaxSettings](../models/client-tax-settings.md)   | :heavy_minus_sign:                                             | N/A                                                            |
| `invoiceRemindersEnabled`                                      | *boolean*                                                      | :heavy_minus_sign:                                             | N/A                                                            |
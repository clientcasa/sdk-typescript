# CatalogItem

## Example Usage

```typescript
import { CatalogItem } from "@clientcasa/sdk/models";

let value: CatalogItem = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  invoiceLabel: "<value>",
  description: "afore weep quirkily hmph where blah inasmuch wasteful",
  invoiceDescription: "<value>",
  defaultRate: 7754.03,
  unit: "flat",
  defaultFrequency: "monthly",
  type: "charge",
  taxCategoryId: "550e8400-e29b-41d4-a716-446655440000",
  status: "paused",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  createdAt: new Date("2024-02-01T18:45:13.705Z"),
  updatedAt: new Date("2024-07-19T15:50:23.231Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `invoiceLabel`                                                                                | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `invoiceDescription`                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `defaultRate`                                                                                 | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `unit`                                                                                        | [models.CatalogItemUnit](../models/catalog-item-unit.md)                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `defaultFrequency`                                                                            | [models.CatalogItemDefaultFrequency](../models/catalog-item-default-frequency.md)             | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `type`                                                                                        | [models.CatalogItemType](../models/catalog-item-type.md)                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `taxCategoryId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `status`                                                                                      | [models.CatalogItemStatus](../models/catalog-item-status.md)                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `clientId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
# Transaction

## Example Usage

```typescript
import { Transaction } from "@clientcasa/sdk/models";

let value: Transaction = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  taxCategoryId: "550e8400-e29b-41d4-a716-446655440000",
  amount: 2655.87,
  frequency: "annual",
  direction: "cost",
  mode: "each",
  splitEvenly: true,
  assignments: [
    {
      projectId: "550e8400-e29b-41d4-a716-446655440000",
      clientId: "550e8400-e29b-41d4-a716-446655440000",
      amount: null,
      percentage: 2964.93,
      fixedAmount: 7840.99,
      startDate: new Date("2024-04-04"),
      endDate: new Date("2025-01-07"),
    },
  ],
  passThrough: true,
  markupPercent: 159.46,
  billedAmount: 5705.74,
  startDate: new Date("2024-08-09"),
  endDate: new Date("2026-05-27"),
  notes: "<value>",
  vendorName: "<value>",
  vendorEmail: "Cleo_Mayer@hotmail.com",
  vendorTaxId: "<id>",
  receiptVerified: false,
  status: "active",
  createdAt: new Date("2026-01-21T05:11:41.607Z"),
  updatedAt: new Date("2026-10-27T20:59:52.770Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `catalogItemId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `taxCategoryId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `amount`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `frequency`                                                                                   | [models.TransactionFrequency](../models/transaction-frequency.md)                             | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `direction`                                                                                   | [models.TransactionDirection](../models/transaction-direction.md)                             | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `mode`                                                                                        | [models.TransactionMode](../models/transaction-mode.md)                                       | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `splitEvenly`                                                                                 | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `assignments`                                                                                 | [models.TransactionAssignment](../models/transaction-assignment.md)[]                         | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `passThrough`                                                                                 | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `markupPercent`                                                                               | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `billedAmount`                                                                                | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `startDate`                                                                                   | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `endDate`                                                                                     | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `notes`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `vendorName`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `vendorEmail`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `vendorTaxId`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `receiptVerified`                                                                             | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | [models.TransactionStatus](../models/transaction-status.md)                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
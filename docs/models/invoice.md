# Invoice

## Example Usage

```typescript
import { Invoice } from "@clientcasa/sdk/models";

let value: Invoice = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  invoiceNumber: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  billingContactId: "550e8400-e29b-41d4-a716-446655440000",
  projectIds: [
    "550e8400-e29b-41d4-a716-446655440000",
  ],
  status: "sent",
  subject: "<value>",
  issueDate: new Date("2025-12-04"),
  dueDate: new Date("2024-08-04"),
  currency: "Tala",
  subtotal: 9683.01,
  discountAmount: 9434.93,
  taxAmount: 5534.8,
  total: 2871.43,
  amountPaid: 1216.19,
  balanceDue: 8377.98,
  paymentTerms: "<value>",
  notes: "<value>",
  paidAt: null,
  lineItems: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      description:
        "questionably house times whether chairperson challenge instead event although helpfully",
      quantity: 7922.87,
      unitPrice: 4824.39,
      taxable: false,
      discountPercent: 6443.54,
      total: 9668.63,
    },
  ],
  createdAt: new Date("2024-02-16T02:08:04.355Z"),
  updatedAt: new Date("2026-09-13T00:11:51.573Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `invoiceNumber`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `clientId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `billingContactId`                                                                            | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `projectIds`                                                                                  | *string*[]                                                                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | [models.InvoiceStatus](../models/invoice-status.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `subject`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `issueDate`                                                                                   | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `dueDate`                                                                                     | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `subtotal`                                                                                    | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `discountAmount`                                                                              | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `taxAmount`                                                                                   | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `total`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `amountPaid`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `balanceDue`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `paymentTerms`                                                                                | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `notes`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `paidAt`                                                                                      | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `lineItems`                                                                                   | [models.InvoiceLineItem](../models/invoice-line-item.md)[]                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
# SaleList

## Example Usage

```typescript
import { SaleList } from "@clientcasa/sdk/models";

let value: SaleList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      saleNumber: "<value>",
      businessId: "550e8400-e29b-41d4-a716-446655440000",
      clientId: "550e8400-e29b-41d4-a716-446655440000",
      contactId: "550e8400-e29b-41d4-a716-446655440000",
      channel: "stripe",
      externalId: "<id>",
      saleDate: new Date("2025-06-04"),
      currency: "Bulgarian Lev",
      status: "completed",
      voidedAt: new Date("2024-07-04T16:42:16.775Z"),
      voidReason: "<value>",
      taxJurisdiction: "<value>",
      taxInclusive: false,
      subtotal: 6940.53,
      discountPercent: 7087.11,
      discountAmount: 4596.99,
      taxRate: 3638.57,
      taxAmount: 7984.59,
      total: 28.39,
      amountRefunded: 2299.11,
      notes: "<value>",
      createdAt: new Date("2026-08-14T19:46:35.770Z"),
      updatedAt: new Date("2025-03-23T04:49:50.943Z"),
    },
  ],
  pagination: {
    page: 299018,
    pageSize: 331897,
    total: 615983,
    totalPages: 226919,
    hasMore: true,
  },
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `data`                                                | [models.Sale](../models/sale.md)[]                    | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
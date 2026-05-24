# PayoutList

## Example Usage

```typescript
import { PayoutList } from "@clientcasa/sdk/models";

let value: PayoutList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      stripePayoutId: "<id>",
      amount: 4115.4,
      currency: "Boliviano boliviano",
      arrivalDate: new Date("2026-08-16"),
      status: "pending",
      type: "<value>",
      automatic: true,
      description:
        "unzip brr recklessly doubtfully intensely institute messy sham or",
      bankAccountLast4: "<value>",
      bankAccountName: "<value>",
      grossTotal: 3161.02,
      feeTotal: 8903.12,
      refundTotal: 1198.3,
      paymentCount: 834569,
      failureCode: null,
      failureMessage: "<value>",
      createdAt: new Date("2025-08-31T13:44:57.802Z"),
      updatedAt: new Date("2025-02-17T12:53:27.702Z"),
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
| `data`                                                | [models.Payout](../models/payout.md)[]                | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
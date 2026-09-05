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
      grossTotal: 0,
      feeTotal: 0,
      refundTotal: 0,
      disputeTotal: 0,
      unattributedTotal: 0,
      paymentCount: 0,
      lastReconciledAt: new Date("2026-08-20T14:32:07.000Z"),
      failureCode: "<value>",
      failureMessage: "<value>",
      createdAt: new Date("2024-05-11T08:00:44.689Z"),
      updatedAt: new Date("2026-07-03T16:30:24.377Z"),
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
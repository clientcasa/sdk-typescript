# RecurringBilling

## Example Usage

```typescript
import { RecurringBilling } from "@clientcasa/sdk/models";

let value: RecurringBilling = {
  status: "pending_setup",
  nextBillingDate: new Date("2025-11-11"),
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `status`                                                               | [models.RecurringBillingStatus](../models/recurring-billing-status.md) | :heavy_check_mark:                                                     | N/A                                                                    |
| `nextBillingDate`                                                      | [Date](../types/rfcdate.md)                                            | :heavy_check_mark:                                                     | N/A                                                                    |
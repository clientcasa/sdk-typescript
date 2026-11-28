# Impact

## Example Usage

```typescript
import { Impact } from "@clientcasa/sdk/models/operations";

let value: Impact = {
  direction: "revenue",
  currency: "Armenian Dram",
  basis: "cash",
  period: "<value>",
  amountCents: 611892,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `direction`                                                                                      | [operations.DeleteTransactionDirection](../../models/operations/delete-transaction-direction.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `currency`                                                                                       | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `basis`                                                                                          | [operations.Basis](../../models/operations/basis.md)                                             | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `period`                                                                                         | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `amountCents`                                                                                    | *number*                                                                                         | :heavy_check_mark:                                                                               | Signed cents removed from the books.                                                             |
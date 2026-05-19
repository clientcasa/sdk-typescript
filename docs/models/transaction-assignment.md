# TransactionAssignment

## Example Usage

```typescript
import { TransactionAssignment } from "@clientcasa/sdk/models";

let value: TransactionAssignment = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  amount: 8785.03,
  percentage: 5800.67,
  fixedAmount: 7297.67,
  startDate: null,
  endDate: new Date("2026-10-31"),
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          | Example                              |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `projectId`                          | *string*                             | :heavy_check_mark:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `clientId`                           | *string*                             | :heavy_check_mark:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `amount`                             | *number*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `percentage`                         | *number*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `fixedAmount`                        | *number*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `startDate`                          | [Date](../types/rfcdate.md)          | :heavy_check_mark:                   | N/A                                  |                                      |
| `endDate`                            | [Date](../types/rfcdate.md)          | :heavy_check_mark:                   | N/A                                  |                                      |
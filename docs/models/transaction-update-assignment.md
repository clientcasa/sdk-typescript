# TransactionUpdateAssignment

## Example Usage

```typescript
import { TransactionUpdateAssignment } from "@clientcasa/sdk/models";

let value: TransactionUpdateAssignment = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          | Example                              |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `projectId`                          | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `clientId`                           | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `amount`                             | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `percentage`                         | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `fixedAmount`                        | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `startDate`                          | [Date](../types/rfcdate.md)          | :heavy_minus_sign:                   | N/A                                  |                                      |
| `endDate`                            | [Date](../types/rfcdate.md)          | :heavy_minus_sign:                   | N/A                                  |                                      |
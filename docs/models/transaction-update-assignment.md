# TransactionUpdateAssignment

## Example Usage

```typescript
import { TransactionUpdateAssignment } from "@clientcasa/sdk/models";

let value: TransactionUpdateAssignment = {
  id: "68b9e3d1c4a2f70012ab34cd",
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              | Example                                  |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `id`                                     | *string*                                 | :heavy_minus_sign:                       | Opaque array-row identifier (not a UUID) | 68b9e3d1c4a2f70012ab34cd                 |
| `projectId`                              | *string*                                 | :heavy_minus_sign:                       | UUID v4                                  | 550e8400-e29b-41d4-a716-446655440000     |
| `clientId`                               | *string*                                 | :heavy_minus_sign:                       | UUID v4                                  | 550e8400-e29b-41d4-a716-446655440000     |
| `amount`                                 | *number*                                 | :heavy_minus_sign:                       | N/A                                      |                                          |
| `percentage`                             | *number*                                 | :heavy_minus_sign:                       | N/A                                      |                                          |
| `fixedAmount`                            | *number*                                 | :heavy_minus_sign:                       | N/A                                      |                                          |
| `startDate`                              | [Date](../types/rfcdate.md)              | :heavy_minus_sign:                       | N/A                                      |                                          |
| `endDate`                                | [Date](../types/rfcdate.md)              | :heavy_minus_sign:                       | N/A                                      |                                          |
| `allocationKey`                          | *string*                                 | :heavy_minus_sign:                       | N/A                                      |                                          |
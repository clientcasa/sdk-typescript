# ListMilestonesRequest

## Example Usage

```typescript
import { ListMilestonesRequest } from "@clientcasa/sdk/models/operations";

let value: ListMilestonesRequest = {
  parentId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `page`                                                                               | *number*                                                                             | :heavy_minus_sign:                                                                   | N/A                                                                                  |                                                                                      |
| `pageSize`                                                                           | *number*                                                                             | :heavy_minus_sign:                                                                   | N/A                                                                                  |                                                                                      |
| `parentType`                                                                         | [operations.ParentType](../../models/operations/parent-type.md)                      | :heavy_minus_sign:                                                                   | N/A                                                                                  |                                                                                      |
| `parentId`                                                                           | *string*                                                                             | :heavy_minus_sign:                                                                   | UUID v4                                                                              | 550e8400-e29b-41d4-a716-446655440000                                                 |
| `status`                                                                             | [operations.ListMilestonesStatus](../../models/operations/list-milestones-status.md) | :heavy_minus_sign:                                                                   | N/A                                                                                  |                                                                                      |
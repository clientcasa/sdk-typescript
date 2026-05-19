# MilestoneCreate

## Example Usage

```typescript
import { MilestoneCreate } from "@clientcasa/sdk/models";

let value: MilestoneCreate = {
  parentType: "proposals",
  parentId: "550e8400-e29b-41d4-a716-446655440000",
  title: "<value>",
  date: new Date("2026-03-20"),
  assigneeId: "550e8400-e29b-41d4-a716-446655440000",
  catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   | Example                                                                       |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `parentType`                                                                  | [models.MilestoneCreateParentType](../models/milestone-create-parent-type.md) | :heavy_check_mark:                                                            | N/A                                                                           |                                                                               |
| `parentId`                                                                    | *string*                                                                      | :heavy_check_mark:                                                            | UUID v4                                                                       | 550e8400-e29b-41d4-a716-446655440000                                          |
| `title`                                                                       | *string*                                                                      | :heavy_check_mark:                                                            | N/A                                                                           |                                                                               |
| `description`                                                                 | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |                                                                               |
| `date`                                                                        | [Date](../types/rfcdate.md)                                                   | :heavy_check_mark:                                                            | N/A                                                                           |                                                                               |
| `time`                                                                        | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |                                                                               |
| `status`                                                                      | [models.MilestoneCreateStatus](../models/milestone-create-status.md)          | :heavy_minus_sign:                                                            | N/A                                                                           |                                                                               |
| `assigneeId`                                                                  | *string*                                                                      | :heavy_minus_sign:                                                            | UUID v4                                                                       | 550e8400-e29b-41d4-a716-446655440000                                          |
| `catalogItemId`                                                               | *string*                                                                      | :heavy_minus_sign:                                                            | UUID v4                                                                       | 550e8400-e29b-41d4-a716-446655440000                                          |
| `sortOrder`                                                                   | *number*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |                                                                               |
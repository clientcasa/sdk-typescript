# Milestone

## Example Usage

```typescript
import { Milestone } from "@clientcasa/sdk/models";

let value: Milestone = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  parentType: "projects",
  parentId: "550e8400-e29b-41d4-a716-446655440000",
  title: "<value>",
  description:
    "remorseful amidst gasp come maestro maul yippee because reassuringly",
  date: new Date("2024-12-07"),
  time: "<value>",
  status: "pending",
  completedAt: new Date("2026-09-22T01:02:05.794Z"),
  assigneeId: "550e8400-e29b-41d4-a716-446655440000",
  catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  sortOrder: 971791,
  createdAt: new Date("2024-06-24T05:12:23.737Z"),
  updatedAt: new Date("2025-06-19T20:53:23.182Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `parentType`                                                                                  | [models.MilestoneParentType](../models/milestone-parent-type.md)                              | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `parentId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `date`                                                                                        | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `time`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | [models.MilestoneStatus](../models/milestone-status.md)                                       | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `completedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `assigneeId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `catalogItemId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `sortOrder`                                                                                   | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
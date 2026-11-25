# Project

## Example Usage

```typescript
import { Project } from "@clientcasa/sdk/models";

let value: Project = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  businessId: "550e8400-e29b-41d4-a716-446655440000",
  status: "completed",
  pipelineStageId: "550e8400-e29b-41d4-a716-446655440000",
  foldedStage: {
    category: "complete",
    state: "updating",
    label: "<value>",
    labelId: "550e8400-e29b-41d4-a716-446655440000",
    status: "paused",
    cancelled: false,
    evidence: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
    commercialAttention: true,
    actualPrecision: "instant",
  },
  startDate: new Date("2026-04-25"),
  endDate: new Date("2026-11-08"),
  eventDate: new Date("2026-03-31"),
  contractValue: 9289.2,
  createdAt: new Date("2024-05-08T18:44:42.561Z"),
  updatedAt: new Date("2026-11-23T18:16:25.118Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `clientId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `businessId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `status`                                                                                      | [models.ProjectStatus](../models/project-status.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `pipelineStageId`                                                                             | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `foldedStage`                                                                                 | [models.FoldedStage](../models/folded-stage.md)                                               | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `startDate`                                                                                   | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `endDate`                                                                                     | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `eventDate`                                                                                   | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `contractValue`                                                                               | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
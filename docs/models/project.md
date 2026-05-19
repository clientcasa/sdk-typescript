# Project

## Example Usage

```typescript
import { Project } from "@clientcasa/sdk/models";

let value: Project = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  name: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  status: "completed",
  pipelineStageId: "550e8400-e29b-41d4-a716-446655440000",
  startDate: new Date("2026-08-21"),
  endDate: new Date("2025-10-30"),
  eventDate: new Date("2026-10-19"),
  contractValue: 1403.97,
  createdAt: new Date("2024-08-20T10:03:50.071Z"),
  updatedAt: new Date("2026-08-23T21:41:05.976Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `clientId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `status`                                                                                      | [models.ProjectStatus](../models/project-status.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `pipelineStageId`                                                                             | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `startDate`                                                                                   | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `endDate`                                                                                     | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `eventDate`                                                                                   | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `contractValue`                                                                               | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
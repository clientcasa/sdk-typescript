# ProjectCreate

## Example Usage

```typescript
import { ProjectCreate } from "@clientcasa/sdk/models";

let value: ProjectCreate = {
  name: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  pipelineStageId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
| `clientId`                                                       | *string*                                                         | :heavy_check_mark:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `status`                                                         | [models.ProjectCreateStatus](../models/project-create-status.md) | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `pipelineStageId`                                                | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `startDate`                                                      | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `endDate`                                                        | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `eventDate`                                                      | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `contractValue`                                                  | *number*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
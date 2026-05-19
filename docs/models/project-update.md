# ProjectUpdate

## Example Usage

```typescript
import { ProjectUpdate } from "@clientcasa/sdk/models";

let value: ProjectUpdate = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  pipelineStageId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `name`                                                           | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `clientId`                                                       | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `status`                                                         | [models.ProjectUpdateStatus](../models/project-update-status.md) | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `pipelineStageId`                                                | *string*                                                         | :heavy_minus_sign:                                               | UUID v4                                                          | 550e8400-e29b-41d4-a716-446655440000                             |
| `startDate`                                                      | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `endDate`                                                        | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `eventDate`                                                      | [Date](../types/rfcdate.md)                                      | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `contractValue`                                                  | *number*                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
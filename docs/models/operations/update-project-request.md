# UpdateProjectRequest

## Example Usage

```typescript
import { UpdateProjectRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateProjectRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    clientId: "550e8400-e29b-41d4-a716-446655440000",
    pipelineStageId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            | Example                                                |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `id`                                                   | *string*                                               | :heavy_check_mark:                                     | UUID v4                                                | 550e8400-e29b-41d4-a716-446655440000                   |
| `body`                                                 | [models.ProjectUpdate](../../models/project-update.md) | :heavy_check_mark:                                     | N/A                                                    |                                                        |
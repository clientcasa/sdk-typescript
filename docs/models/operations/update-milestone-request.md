# UpdateMilestoneRequest

## Example Usage

```typescript
import { UpdateMilestoneRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateMilestoneRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    assigneeId: "550e8400-e29b-41d4-a716-446655440000",
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                | Example                                                    |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `id`                                                       | *string*                                                   | :heavy_check_mark:                                         | UUID v4                                                    | 550e8400-e29b-41d4-a716-446655440000                       |
| `body`                                                     | [models.MilestoneUpdate](../../models/milestone-update.md) | :heavy_check_mark:                                         | N/A                                                        |                                                            |
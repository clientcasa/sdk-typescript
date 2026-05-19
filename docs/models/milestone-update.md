# MilestoneUpdate

## Example Usage

```typescript
import { MilestoneUpdate } from "@clientcasa/sdk/models";

let value: MilestoneUpdate = {
  assigneeId: "550e8400-e29b-41d4-a716-446655440000",
  catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          | Example                                                              |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `title`                                                              | *string*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |                                                                      |
| `description`                                                        | *string*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |                                                                      |
| `date`                                                               | [Date](../types/rfcdate.md)                                          | :heavy_minus_sign:                                                   | N/A                                                                  |                                                                      |
| `time`                                                               | *string*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |                                                                      |
| `status`                                                             | [models.MilestoneUpdateStatus](../models/milestone-update-status.md) | :heavy_minus_sign:                                                   | N/A                                                                  |                                                                      |
| `assigneeId`                                                         | *string*                                                             | :heavy_minus_sign:                                                   | UUID v4                                                              | 550e8400-e29b-41d4-a716-446655440000                                 |
| `catalogItemId`                                                      | *string*                                                             | :heavy_minus_sign:                                                   | UUID v4                                                              | 550e8400-e29b-41d4-a716-446655440000                                 |
| `sortOrder`                                                          | *number*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |                                                                      |
# TimeEntryUpdate

## Example Usage

```typescript
import { TimeEntryUpdate } from "@clientcasa/sdk/models";

let value: TimeEntryUpdate = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  memberId: "550e8400-e29b-41d4-a716-446655440000",
  catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                | Example                                                                    |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `projectId`                                                                | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `memberId`                                                                 | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `catalogItemId`                                                            | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `date`                                                                     | [Date](../types/rfcdate.md)                                                | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `hours`                                                                    | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `description`                                                              | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `billable`                                                                 | *boolean*                                                                  | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `rateType`                                                                 | [models.TimeEntryUpdateRateType](../models/time-entry-update-rate-type.md) | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `customMultiplierName`                                                     | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `rateOverride`                                                             | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `workerName`                                                               | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
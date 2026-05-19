# TimeEntryCreate

## Example Usage

```typescript
import { TimeEntryCreate } from "@clientcasa/sdk/models";

let value: TimeEntryCreate = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  memberId: "550e8400-e29b-41d4-a716-446655440000",
  catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  date: new Date("2024-09-01"),
  hours: 2026.81,
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                | Example                                                                    |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `projectId`                                                                | *string*                                                                   | :heavy_check_mark:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `memberId`                                                                 | *string*                                                                   | :heavy_check_mark:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `catalogItemId`                                                            | *string*                                                                   | :heavy_minus_sign:                                                         | UUID v4                                                                    | 550e8400-e29b-41d4-a716-446655440000                                       |
| `date`                                                                     | [Date](../types/rfcdate.md)                                                | :heavy_check_mark:                                                         | N/A                                                                        |                                                                            |
| `hours`                                                                    | *number*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |                                                                            |
| `description`                                                              | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `billable`                                                                 | *boolean*                                                                  | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `rateType`                                                                 | [models.TimeEntryCreateRateType](../models/time-entry-create-rate-type.md) | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `customMultiplierName`                                                     | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `rateOverride`                                                             | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `discountPercent`                                                          | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
| `workerName`                                                               | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |                                                                            |
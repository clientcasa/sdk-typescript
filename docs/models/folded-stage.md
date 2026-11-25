# FoldedStage

## Example Usage

```typescript
import { FoldedStage } from "@clientcasa/sdk/models";

let value: FoldedStage = {
  category: "booked",
  state: "updating",
  label: "<value>",
  labelId: "550e8400-e29b-41d4-a716-446655440000",
  status: "paused",
  cancelled: true,
  evidence: [
    "<value 1>",
  ],
  commercialAttention: false,
  actualPrecision: "unknown",
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  | Example                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `category`                                                   | [models.Category](../models/category.md)                     | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `state`                                                      | [models.State](../models/state.md)                           | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `label`                                                      | *string*                                                     | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `labelId`                                                    | *string*                                                     | :heavy_check_mark:                                           | UUID v4                                                      | 550e8400-e29b-41d4-a716-446655440000                         |
| `status`                                                     | [models.FoldedStageStatus](../models/folded-stage-status.md) | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `cancelled`                                                  | *boolean*                                                    | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `evidence`                                                   | *string*[]                                                   | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `commercialAttention`                                        | *boolean*                                                    | :heavy_check_mark:                                           | N/A                                                          |                                                              |
| `actualPrecision`                                            | [models.ActualPrecision](../models/actual-precision.md)      | :heavy_check_mark:                                           | N/A                                                          |                                                              |
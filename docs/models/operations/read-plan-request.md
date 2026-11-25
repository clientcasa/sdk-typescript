# ReadPlanRequest

## Example Usage

```typescript
import { ReadPlanRequest } from "@clientcasa/sdk/models/operations";

let value: ReadPlanRequest = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  eventDayId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              | Example                                                                  |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `projectId`                                                              | *string*                                                                 | :heavy_minus_sign:                                                       | UUID v4                                                                  | 550e8400-e29b-41d4-a716-446655440000                                     |
| `clientId`                                                               | *string*                                                                 | :heavy_minus_sign:                                                       | UUID v4                                                                  | 550e8400-e29b-41d4-a716-446655440000                                     |
| `scope`                                                                  | [operations.ReadPlanScope](../../models/operations/read-plan-scope.md)   | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
| `eventDayId`                                                             | *string*                                                                 | :heavy_minus_sign:                                                       | UUID v4                                                                  | 550e8400-e29b-41d4-a716-446655440000                                     |
| `mode`                                                                   | [operations.ReadPlanMode](../../models/operations/read-plan-mode.md)     | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
| `start`                                                                  | [Date](../../types/rfcdate.md)                                           | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
| `end`                                                                    | [Date](../../types/rfcdate.md)                                           | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
| `after`                                                                  | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
| `limit`                                                                  | *number*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
| `kind`                                                                   | [operations.ReadPlanKind](../../models/operations/read-plan-kind.md)     | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
| `status`                                                                 | [operations.ReadPlanStatus](../../models/operations/read-plan-status.md) | :heavy_minus_sign:                                                       | N/A                                                                      |                                                                          |
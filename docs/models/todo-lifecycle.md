# TodoLifecycle

## Example Usage

```typescript
import { TodoLifecycle } from "@clientcasa/sdk/models";

let value: TodoLifecycle = {
  commandId: "550e8400-e29b-41d4-a716-446655440000",
  expectedRevision: 622678,
  billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   | Example                                       |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `commandId`                                   | *string*                                      | :heavy_check_mark:                            | UUID v4                                       | 550e8400-e29b-41d4-a716-446655440000          |
| `expectedRevision`                            | *number*                                      | :heavy_check_mark:                            | N/A                                           |                                               |
| `billingReviewId`                             | *string*                                      | :heavy_minus_sign:                            | UUID v4                                       | 550e8400-e29b-41d4-a716-446655440000          |
| `dateChoice`                                  | [models.DateChoice](../models/date-choice.md) | :heavy_minus_sign:                            | N/A                                           |                                               |
| `reason`                                      | *string*                                      | :heavy_minus_sign:                            | N/A                                           |                                               |
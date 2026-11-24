# TodoCreateDeadlineRuleEventRelative

## Example Usage

```typescript
import { TodoCreateDeadlineRuleEventRelative } from "@clientcasa/sdk/models";

let value: TodoCreateDeadlineRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 511127,
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `kind`                                     | *"event-relative"*                         | :heavy_check_mark:                         | N/A                                        |
| `anchor`                                   | *models.TodoCreateDeadlineRuleAnchorUnion* | :heavy_check_mark:                         | N/A                                        |
| `offsetDays`                               | *number*                                   | :heavy_check_mark:                         | N/A                                        |
| `localTime`                                | *string*                                   | :heavy_minus_sign:                         | N/A                                        |
| `zone`                                     | *string*                                   | :heavy_minus_sign:                         | N/A                                        |
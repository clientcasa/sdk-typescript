# TodoUpdateDeadlineRuleEventRelative

## Example Usage

```typescript
import { TodoUpdateDeadlineRuleEventRelative } from "@clientcasa/sdk/models";

let value: TodoUpdateDeadlineRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 522484,
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `kind`                                     | *"event-relative"*                         | :heavy_check_mark:                         | N/A                                        |
| `anchor`                                   | *models.TodoUpdateDeadlineRuleAnchorUnion* | :heavy_check_mark:                         | N/A                                        |
| `offsetDays`                               | *number*                                   | :heavy_check_mark:                         | N/A                                        |
| `localTime`                                | *string*                                   | :heavy_minus_sign:                         | N/A                                        |
| `zone`                                     | *string*                                   | :heavy_minus_sign:                         | N/A                                        |
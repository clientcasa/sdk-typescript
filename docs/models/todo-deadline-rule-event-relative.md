# TodoDeadlineRuleEventRelative

## Example Usage

```typescript
import { TodoDeadlineRuleEventRelative } from "@clientcasa/sdk/models";

let value: TodoDeadlineRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 866946,
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `kind`                               | *"event-relative"*                   | :heavy_check_mark:                   | N/A                                  |
| `anchor`                             | *models.TodoDeadlineRuleAnchorUnion* | :heavy_check_mark:                   | N/A                                  |
| `offsetDays`                         | *number*                             | :heavy_check_mark:                   | N/A                                  |
| `localTime`                          | *string*                             | :heavy_minus_sign:                   | N/A                                  |
| `zone`                               | *string*                             | :heavy_minus_sign:                   | N/A                                  |
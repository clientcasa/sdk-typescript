# TodoCreateDoRuleEventRelative

## Example Usage

```typescript
import { TodoCreateDoRuleEventRelative } from "@clientcasa/sdk/models";

let value: TodoCreateDoRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "1cf81fd4-2414-45bc-975f-c819d864562a",
  },
  offsetDays: 727984,
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `kind`                               | *"event-relative"*                   | :heavy_check_mark:                   | N/A                                  |
| `anchor`                             | *models.TodoCreateDoRuleAnchorUnion* | :heavy_check_mark:                   | N/A                                  |
| `offsetDays`                         | *number*                             | :heavy_check_mark:                   | N/A                                  |
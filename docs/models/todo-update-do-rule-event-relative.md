# TodoUpdateDoRuleEventRelative

## Example Usage

```typescript
import { TodoUpdateDoRuleEventRelative } from "@clientcasa/sdk/models";

let value: TodoUpdateDoRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "cc736a2b-17b6-4552-81da-d2bdbd106e49",
  },
  offsetDays: 637998,
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `kind`                               | *"event-relative"*                   | :heavy_check_mark:                   | N/A                                  |
| `anchor`                             | *models.TodoUpdateDoRuleAnchorUnion* | :heavy_check_mark:                   | N/A                                  |
| `offsetDays`                         | *number*                             | :heavy_check_mark:                   | N/A                                  |
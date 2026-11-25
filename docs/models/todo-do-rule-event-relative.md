# TodoDoRuleEventRelative

## Example Usage

```typescript
import { TodoDoRuleEventRelative } from "@clientcasa/sdk/models";

let value: TodoDoRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 541823,
};
```

## Fields

| Field                          | Type                           | Required                       | Description                    |
| ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ |
| `kind`                         | *"event-relative"*             | :heavy_check_mark:             | N/A                            |
| `anchor`                       | *models.TodoDoRuleAnchorUnion* | :heavy_check_mark:             | N/A                            |
| `offsetDays`                   | *number*                       | :heavy_check_mark:             | N/A                            |
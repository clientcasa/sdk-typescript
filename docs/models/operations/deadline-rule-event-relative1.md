# DeadlineRuleEventRelative1

## Example Usage

```typescript
import { DeadlineRuleEventRelative1 } from "@clientcasa/sdk/models/operations";

let value: DeadlineRuleEventRelative1 = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "e62cb379-d340-4fad-becb-2d59156b6e73",
  },
  offsetDays: 452406,
};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `kind`                                | *"event-relative"*                    | :heavy_check_mark:                    | N/A                                   |
| `anchor`                              | *operations.DeadlineRuleAnchorUnion1* | :heavy_check_mark:                    | N/A                                   |
| `offsetDays`                          | *number*                              | :heavy_check_mark:                    | N/A                                   |
| `localTime`                           | *string*                              | :heavy_minus_sign:                    | N/A                                   |
| `zone`                                | *string*                              | :heavy_minus_sign:                    | N/A                                   |
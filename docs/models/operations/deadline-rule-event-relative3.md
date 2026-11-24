# DeadlineRuleEventRelative3

## Example Usage

```typescript
import { DeadlineRuleEventRelative3 } from "@clientcasa/sdk/models/operations";

let value: DeadlineRuleEventRelative3 = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 562586,
};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `kind`                                | *"event-relative"*                    | :heavy_check_mark:                    | N/A                                   |
| `anchor`                              | *operations.DeadlineRuleAnchorUnion3* | :heavy_check_mark:                    | N/A                                   |
| `offsetDays`                          | *number*                              | :heavy_check_mark:                    | N/A                                   |
| `localTime`                           | *string*                              | :heavy_minus_sign:                    | N/A                                   |
| `zone`                                | *string*                              | :heavy_minus_sign:                    | N/A                                   |
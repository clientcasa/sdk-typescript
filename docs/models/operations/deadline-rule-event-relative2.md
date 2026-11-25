# DeadlineRuleEventRelative2

## Example Usage

```typescript
import { DeadlineRuleEventRelative2 } from "@clientcasa/sdk/models/operations";

let value: DeadlineRuleEventRelative2 = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 615302,
};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `kind`                                | *"event-relative"*                    | :heavy_check_mark:                    | N/A                                   |
| `anchor`                              | *operations.DeadlineRuleAnchorUnion2* | :heavy_check_mark:                    | N/A                                   |
| `offsetDays`                          | *number*                              | :heavy_check_mark:                    | N/A                                   |
| `localTime`                           | *string*                              | :heavy_minus_sign:                    | N/A                                   |
| `zone`                                | *string*                              | :heavy_minus_sign:                    | N/A                                   |
# DoRuleEventRelative2

## Example Usage

```typescript
import { DoRuleEventRelative2 } from "@clientcasa/sdk/models/operations";

let value: DoRuleEventRelative2 = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 240360,
};
```

## Fields

| Field                           | Type                            | Required                        | Description                     |
| ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| `kind`                          | *"event-relative"*              | :heavy_check_mark:              | N/A                             |
| `anchor`                        | *operations.DoRuleAnchorUnion2* | :heavy_check_mark:              | N/A                             |
| `offsetDays`                    | *number*                        | :heavy_check_mark:              | N/A                             |
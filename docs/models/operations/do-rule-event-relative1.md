# DoRuleEventRelative1

## Example Usage

```typescript
import { DoRuleEventRelative1 } from "@clientcasa/sdk/models/operations";

let value: DoRuleEventRelative1 = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "47f18ccb-0f58-4ac4-a654-99063278832d",
  },
  offsetDays: 896804,
};
```

## Fields

| Field                           | Type                            | Required                        | Description                     |
| ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| `kind`                          | *"event-relative"*              | :heavy_check_mark:              | N/A                             |
| `anchor`                        | *operations.DoRuleAnchorUnion1* | :heavy_check_mark:              | N/A                             |
| `offsetDays`                    | *number*                        | :heavy_check_mark:              | N/A                             |
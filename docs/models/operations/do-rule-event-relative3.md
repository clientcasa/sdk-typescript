# DoRuleEventRelative3

## Example Usage

```typescript
import { DoRuleEventRelative3 } from "@clientcasa/sdk/models/operations";

let value: DoRuleEventRelative3 = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "179fb2f0-8c74-4710-b749-cc8bcb3fad2c",
  },
  offsetDays: 850403,
};
```

## Fields

| Field                           | Type                            | Required                        | Description                     |
| ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| `kind`                          | *"event-relative"*              | :heavy_check_mark:              | N/A                             |
| `anchor`                        | *operations.DoRuleAnchorUnion3* | :heavy_check_mark:              | N/A                             |
| `offsetDays`                    | *number*                        | :heavy_check_mark:              | N/A                             |
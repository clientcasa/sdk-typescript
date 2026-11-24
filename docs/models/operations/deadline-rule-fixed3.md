# DeadlineRuleFixed3

## Example Usage

```typescript
import { DeadlineRuleFixed3 } from "@clientcasa/sdk/models/operations";

let value: DeadlineRuleFixed3 = {
  kind: "fixed",
  day: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `kind`             | *"fixed"*          | :heavy_check_mark: | N/A                |
| `day`              | *string*           | :heavy_check_mark: | N/A                |
| `localTime`        | *string*           | :heavy_minus_sign: | N/A                |
| `zone`             | *string*           | :heavy_minus_sign: | N/A                |
# DeadlineRuleFixed2

## Example Usage

```typescript
import { DeadlineRuleFixed2 } from "@clientcasa/sdk/models/operations";

let value: DeadlineRuleFixed2 = {
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
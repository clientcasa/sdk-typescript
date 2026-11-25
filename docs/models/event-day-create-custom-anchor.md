# EventDayCreateCustomAnchor

## Example Usage

```typescript
import { EventDayCreateCustomAnchor } from "@clientcasa/sdk/models";

let value: EventDayCreateCustomAnchor = {
  key: "<key>",
  time: "16:07",
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            | Example                                                                                                |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `key`                                                                                                  | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |                                                                                                        |
| `label`                                                                                                | *string*                                                                                               | :heavy_minus_sign:                                                                                     | N/A                                                                                                    |                                                                                                        |
| `time`                                                                                                 | *string*                                                                                               | :heavy_minus_sign:                                                                                     | Local time in HH:mm (24-hour), from 00:00 to 23:59, or no value to leave it unset. No seconds or date. | 16:07                                                                                                  |
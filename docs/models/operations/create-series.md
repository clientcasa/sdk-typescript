# CreateSeries

## Example Usage

```typescript
import { CreateSeries } from "@clientcasa/sdk/models/operations";

let value: CreateSeries = {
  intent: "create-series",
  commandId: "5dc0df39-f2b0-44fe-9fad-7133acbe5818",
  seriesId: "09182150-fb8c-48a4-a1ab-2149a5283fc6",
  businessId: "4d97f589-ee8e-41d1-8660-30960bcdca0b",
  title: "<value>",
  rrule: "<value>",
  day: "<value>",
  fields: {},
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `intent`                                                 | *"create-series"*                                        | :heavy_check_mark:                                       | N/A                                                      |
| `commandId`                                              | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `seriesId`                                               | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `businessId`                                             | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `projectId`                                              | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `clientId`                                               | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `title`                                                  | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `rrule`                                                  | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `day`                                                    | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `fields`                                                 | [operations.Fields1](../../models/operations/fields1.md) | :heavy_check_mark:                                       | N/A                                                      |
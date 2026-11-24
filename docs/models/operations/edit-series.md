# EditSeries

## Example Usage

```typescript
import { EditSeries } from "@clientcasa/sdk/models/operations";

let value: EditSeries = {
  intent: "edit-series",
  commandId: "728f0b47-f39c-4086-94a8-6003f1bd811f",
  seriesId: "886648fc-826d-46be-8eb1-6e37e65b015b",
  newSeriesId: "3857c0d3-ecd5-4770-91ba-594a3993c8e3",
  nominalKey: "<value>",
  expectedUpdatedAt: "<value>",
  expectedLineageVersion: "<value>",
  scope: "future",
  reviewed: true,
  fields: {},
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `intent`                                                                                        | *"edit-series"*                                                                                 | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `commandId`                                                                                     | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `seriesId`                                                                                      | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `newSeriesId`                                                                                   | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `nominalKey`                                                                                    | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `expectedUpdatedAt`                                                                             | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `expectedLineageVersion`                                                                        | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `scope`                                                                                         | [operations.ChangeTodoOccurrenceScope](../../models/operations/change-todo-occurrence-scope.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `reviewed`                                                                                      | *true*                                                                                          | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `fields`                                                                                        | [operations.Fields3](../../models/operations/fields3.md)                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
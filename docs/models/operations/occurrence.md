# Occurrence

## Example Usage

```typescript
import { Occurrence } from "@clientcasa/sdk/models/operations";

let value: Occurrence = {
  intent: "occurrence",
  commandId: "17d94d11-461e-46da-90c3-210da736b88a",
  seriesId: "528b3a49-5134-4cab-b79a-0d49212793e5",
  nominalKey: "<value>",
  expectedRevision: 503043,
  todoId: "3298f793-8e32-4103-91cd-ae98c199fc89",
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `intent`                                                 | *"occurrence"*                                           | :heavy_check_mark:                                       | N/A                                                      |
| `commandId`                                              | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `seriesId`                                               | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `nominalKey`                                             | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `expectedRevision`                                       | *number*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `todoId`                                                 | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `fields`                                                 | [operations.Fields2](../../models/operations/fields2.md) | :heavy_minus_sign:                                       | N/A                                                      |
| `action`                                                 | [operations.Action](../../models/operations/action.md)   | :heavy_minus_sign:                                       | N/A                                                      |
| `reason`                                                 | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
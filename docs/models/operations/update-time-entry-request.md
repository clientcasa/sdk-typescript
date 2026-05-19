# UpdateTimeEntryRequest

## Example Usage

```typescript
import { UpdateTimeEntryRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateTimeEntryRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    projectId: "550e8400-e29b-41d4-a716-446655440000",
    memberId: "550e8400-e29b-41d4-a716-446655440000",
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 | Example                                                     |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `id`                                                        | *string*                                                    | :heavy_check_mark:                                          | UUID v4                                                     | 550e8400-e29b-41d4-a716-446655440000                        |
| `body`                                                      | [models.TimeEntryUpdate](../../models/time-entry-update.md) | :heavy_check_mark:                                          | N/A                                                         |                                                             |
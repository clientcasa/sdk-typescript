# ChangeTodoOccurrenceRequest

## Example Usage

```typescript
import { ChangeTodoOccurrenceRequest } from "@clientcasa/sdk/models/operations";

let value: ChangeTodoOccurrenceRequest = {
  idempotencyKey: "create-client-2026-05-24-a1b2c3",
  body: {
    intent: "edit-series",
    commandId: "17140f8a-b19f-4197-9a44-d3dd51871124",
    seriesId: "8d5bf196-749e-4806-be08-782b8b89ee9f",
    newSeriesId: "ff51fac4-63bc-4c86-9daa-942c0710c7ba",
    nominalKey: "<value>",
    expectedUpdatedAt: "<value>",
    expectedLineageVersion: "<value>",
    scope: "future",
    reviewed: true,
    fields: {},
  },
};
```

## Fields

| Field                                                                                                                                                                                                        | Type                                                                                                                                                                                                         | Required                                                                                                                                                                                                     | Description                                                                                                                                                                                                  | Example                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `idempotencyKey`                                                                                                                                                                                             | *string*                                                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                           | Optional unique key that makes this request safely retryable. Replaying the same key returns the original response instead of creating a duplicate; reusing a key with a different request body returns 409. | create-client-2026-05-24-a1b2c3                                                                                                                                                                              |
| `body`                                                                                                                                                                                                       | *operations.ChangeTodoOccurrenceRequestBody*                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                           | N/A                                                                                                                                                                                                          |                                                                                                                                                                                                              |
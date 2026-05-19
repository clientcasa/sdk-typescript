# ListTimeEntriesRequest

## Example Usage

```typescript
import { ListTimeEntriesRequest } from "@clientcasa/sdk/models/operations";

let value: ListTimeEntriesRequest = {
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  memberId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          | Example                              |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `page`                               | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `pageSize`                           | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `projectId`                          | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `clientId`                           | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `memberId`                           | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `dateFrom`                           | [Date](../../types/rfcdate.md)       | :heavy_minus_sign:                   | N/A                                  |                                      |
| `dateTo`                             | [Date](../../types/rfcdate.md)       | :heavy_minus_sign:                   | N/A                                  |                                      |
| `billable`                           | *boolean*                            | :heavy_minus_sign:                   | N/A                                  |                                      |
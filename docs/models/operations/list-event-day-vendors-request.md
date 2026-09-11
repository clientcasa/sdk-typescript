# ListEventDayVendorsRequest

## Example Usage

```typescript
import { ListEventDayVendorsRequest } from "@clientcasa/sdk/models/operations";

let value: ListEventDayVendorsRequest = {
  eventDayId: "550e8400-e29b-41d4-a716-446655440000",
  vendorId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          | Example                              |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `page`                               | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `pageSize`                           | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |
| `eventDayId`                         | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `vendorId`                           | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
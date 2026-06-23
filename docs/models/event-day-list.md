# EventDayList

## Example Usage

```typescript
import { EventDayList } from "@clientcasa/sdk/models";

let value: EventDayList = {
  data: [],
  pagination: {
    page: 299018,
    pageSize: 331897,
    total: 615983,
    totalPages: 226919,
    hasMore: true,
  },
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `data`                                                | [models.EventDay](../models/event-day.md)[]           | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
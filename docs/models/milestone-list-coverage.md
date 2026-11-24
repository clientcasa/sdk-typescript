# MilestoneListCoverage

## Example Usage

```typescript
import { MilestoneListCoverage } from "@clientcasa/sdk/models";

let value: MilestoneListCoverage = {
  after: "<value>",
  next: "<value>",
  stopped: false,
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `after`                                                           | *string*                                                          | :heavy_check_mark:                                                | Opaque date and identity continuation from pagination.nextCursor. |
| `next`                                                            | *string*                                                          | :heavy_check_mark:                                                | Opaque date and identity continuation from pagination.nextCursor. |
| `stopped`                                                         | *boolean*                                                         | :heavy_check_mark:                                                | N/A                                                               |
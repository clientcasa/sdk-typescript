# MilestoneCursorPagination

## Example Usage

```typescript
import { MilestoneCursorPagination } from "@clientcasa/sdk/models";

let value: MilestoneCursorPagination = {
  page: 975142,
  pageSize: 365196,
  total: 1131,
  totalPages: 249778,
  hasMore: true,
  nextCursor: "<value>",
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `page`                                                            | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `pageSize`                                                        | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `total`                                                           | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `totalPages`                                                      | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `hasMore`                                                         | *boolean*                                                         | :heavy_check_mark:                                                | N/A                                                               |
| `nextCursor`                                                      | *string*                                                          | :heavy_check_mark:                                                | Opaque date and identity continuation from pagination.nextCursor. |
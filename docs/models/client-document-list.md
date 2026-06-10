# ClientDocumentList

## Example Usage

```typescript
import { ClientDocumentList } from "@clientcasa/sdk/models";

let value: ClientDocumentList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      kind: "smart-file",
      title: "<value>",
      status: "expired",
      contactId: "550e8400-e29b-41d4-a716-446655440000",
      clientId: "550e8400-e29b-41d4-a716-446655440000",
      projectId: "550e8400-e29b-41d4-a716-446655440000",
      engagementProjectId: "550e8400-e29b-41d4-a716-446655440000",
      isTemplate: false,
      clientUrl: "https://feline-shadowbox.com/",
      quoteConvertedAt: new Date("2025-08-12T13:21:28.001Z"),
      expiresAt: null,
      createdAt: new Date("2026-08-14T23:18:20.625Z"),
      updatedAt: new Date("2025-12-13T16:08:13.937Z"),
    },
  ],
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

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `data`                                                  | [models.ClientDocument](../models/client-document.md)[] | :heavy_check_mark:                                      | N/A                                                     |
| `pagination`                                            | [models.PaginationMeta](../models/pagination-meta.md)   | :heavy_check_mark:                                      | N/A                                                     |
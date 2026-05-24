# InquiryList

## Example Usage

```typescript
import { InquiryList } from "@clientcasa/sdk/models";

let value: InquiryList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      name: "<value>",
      email: "Sydnie.Boyer6@hotmail.com",
      phone: "843-469-9006 x6952",
      contactId: "550e8400-e29b-41d4-a716-446655440000",
      inquirySlug: "<value>",
      preferredDate: new Date("2026-09-30"),
      message: null,
      status: "contacted",
      source: "other",
      customAnswers: null,
      convertedClientId: "550e8400-e29b-41d4-a716-446655440000",
      convertedProjectId: "550e8400-e29b-41d4-a716-446655440000",
      convertedAt: null,
      lastContactedAt: new Date("2024-05-27T03:42:31.110Z"),
      nextFollowUpAt: new Date("2025-08-26T21:14:11.899Z"),
      notes: "<value>",
      createdAt: new Date("2026-10-19T13:55:15.621Z"),
      updatedAt: new Date("2026-07-01T19:53:51.099Z"),
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

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `data`                                                | [models.Inquiry](../models/inquiry.md)[]              | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
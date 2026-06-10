# ContactList

## Example Usage

```typescript
import { ContactList } from "@clientcasa/sdk/models";

let value: ContactList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      name: "<value>",
      email: "Arjun.Goodwin@gmail.com",
      phone: "982-868-6018 x9210",
      title: "<value>",
      role: "billing",
      isPrimary: true,
      clientId: "550e8400-e29b-41d4-a716-446655440000",
      sourceSubmissionId: "550e8400-e29b-41d4-a716-446655440000",
      createdAt: new Date("2026-01-15T03:20:43.958Z"),
      updatedAt: new Date("2025-04-26T09:41:35.455Z"),
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
| `data`                                                | [models.Contact](../models/contact.md)[]              | :heavy_check_mark:                                    | N/A                                                   |
| `pagination`                                          | [models.PaginationMeta](../models/pagination-meta.md) | :heavy_check_mark:                                    | N/A                                                   |
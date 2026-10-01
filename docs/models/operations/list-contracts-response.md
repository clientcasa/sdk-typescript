# ListContractsResponse

## Example Usage

```typescript
import { ListContractsResponse } from "@clientcasa/sdk/models/operations";

let value: ListContractsResponse = {
  result: {
    data: [
      {
        id: "550e8400-e29b-41d4-a716-446655440000",
        contractNumber: "<value>",
        title: "<value>",
        clientId: "550e8400-e29b-41d4-a716-446655440000",
        billingContactId: "550e8400-e29b-41d4-a716-446655440000",
        projectId: "550e8400-e29b-41d4-a716-446655440000",
        sourceTemplateId: "550e8400-e29b-41d4-a716-446655440000",
        status: "expired",
        contentType: "tiptap",
        issueDate: new Date("2025-11-28"),
        effectiveDate: null,
        expirationDate: new Date("2026-07-16"),
        signedDate: new Date("2026-11-05T07:18:07.688Z"),
        currency: "Saudi Riyal",
        contractValue: 9288.27,
        signers: [
          {
            contactId: "550e8400-e29b-41d4-a716-446655440000",
            name: "<value>",
            email: "",
            role: "<value>",
            order: 934500,
            status: "<value>",
            signedAt: new Date("2026-03-21T16:10:44.851Z"),
          },
        ],
        archived: false,
        archivedAt: new Date("2024-09-15T00:04:58.879Z"),
        createdAt: new Date("2026-10-07T04:22:23.354Z"),
        updatedAt: new Date("2024-05-14T18:34:05.240Z"),
      },
    ],
    pagination: {
      page: 299018,
      pageSize: 331897,
      total: 615983,
      totalPages: 226919,
      hasMore: true,
    },
  },
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `result`                                             | [models.ContractList](../../models/contract-list.md) | :heavy_check_mark:                                   | N/A                                                  |
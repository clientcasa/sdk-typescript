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
        proposalId: "550e8400-e29b-41d4-a716-446655440000",
        projectId: "550e8400-e29b-41d4-a716-446655440000",
        sourceTemplateId: "550e8400-e29b-41d4-a716-446655440000",
        status: "expired",
        signingMode: "counter_sign",
        contentType: "pdf",
        issueDate: new Date("2024-04-11"),
        effectiveDate: new Date("2026-07-16"),
        expirationDate: new Date("2026-11-05"),
        signedDate: new Date("2025-07-26T20:33:11.897Z"),
        currency: "Tala",
        contractValue: 6403.57,
        signers: [
          {
            contactId: "550e8400-e29b-41d4-a716-446655440000",
            name: "<value>",
            email: "",
            role: "<value>",
            order: 739666,
            status: "<value>",
            signedAt: new Date("2026-07-04T14:07:50.771Z"),
          },
        ],
        archived: true,
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
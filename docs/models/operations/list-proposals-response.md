# ListProposalsResponse

## Example Usage

```typescript
import { ListProposalsResponse } from "@clientcasa/sdk/models/operations";

let value: ListProposalsResponse = {
  result: {
    data: [
      {
        id: "550e8400-e29b-41d4-a716-446655440000",
        proposalNumber: "<value>",
        title: "<value>",
        clientId: "550e8400-e29b-41d4-a716-446655440000",
        billingContactId: "550e8400-e29b-41d4-a716-446655440000",
        projectId: "550e8400-e29b-41d4-a716-446655440000",
        status: "draft",
        sendMode: "agreement",
        issueDate: new Date("2026-04-08"),
        expirationDate: new Date("2025-08-08"),
        eventDate: new Date("2024-12-02"),
        currency: "Guarani",
        subtotal: 3924.48,
        discountAmount: 6638.75,
        taxAmount: 4064.03,
        total: 171.22,
        notes: "<value>",
        archived: true,
        linkedContractId: "550e8400-e29b-41d4-a716-446655440000",
        createdAt: new Date("2026-06-10T10:33:16.115Z"),
        updatedAt: new Date("2026-08-29T00:11:16.733Z"),
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
| `result`                                             | [models.ProposalList](../../models/proposal-list.md) | :heavy_check_mark:                                   | N/A                                                  |
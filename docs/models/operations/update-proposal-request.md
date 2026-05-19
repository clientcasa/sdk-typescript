# UpdateProposalRequest

## Example Usage

```typescript
import { UpdateProposalRequest } from "@clientcasa/sdk/models/operations";

let value: UpdateProposalRequest = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  body: {
    billingContactId: "550e8400-e29b-41d4-a716-446655440000",
    projectId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `id`                                                     | *string*                                                 | :heavy_check_mark:                                       | UUID v4                                                  | 550e8400-e29b-41d4-a716-446655440000                     |
| `body`                                                   | [models.ProposalUpdate](../../models/proposal-update.md) | :heavy_check_mark:                                       | N/A                                                      |                                                          |
# ProposalUpdate

## Example Usage

```typescript
import { ProposalUpdate } from "@clientcasa/sdk/models";

let value: ProposalUpdate = {
  billingContactId: "550e8400-e29b-41d4-a716-446655440000",
  projectId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        | Example                                                            |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `title`                                                            | *string*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |                                                                    |
| `billingContactId`                                                 | *string*                                                           | :heavy_minus_sign:                                                 | UUID v4                                                            | 550e8400-e29b-41d4-a716-446655440000                               |
| `projectId`                                                        | *string*                                                           | :heavy_minus_sign:                                                 | UUID v4                                                            | 550e8400-e29b-41d4-a716-446655440000                               |
| `status`                                                           | [models.ProposalUpdateStatus](../models/proposal-update-status.md) | :heavy_minus_sign:                                                 | N/A                                                                |                                                                    |
| `issueDate`                                                        | [Date](../types/rfcdate.md)                                        | :heavy_minus_sign:                                                 | N/A                                                                |                                                                    |
| `expirationDate`                                                   | [Date](../types/rfcdate.md)                                        | :heavy_minus_sign:                                                 | N/A                                                                |                                                                    |
| `eventDate`                                                        | [Date](../types/rfcdate.md)                                        | :heavy_minus_sign:                                                 | N/A                                                                |                                                                    |
| `notes`                                                            | *string*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |                                                                    |
| `archived`                                                         | *boolean*                                                          | :heavy_minus_sign:                                                 | N/A                                                                |                                                                    |
# ProposalCreate

## Example Usage

```typescript
import { ProposalCreate } from "@clientcasa/sdk/models";

let value: ProposalCreate = {
  title: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  billingContactId: "550e8400-e29b-41d4-a716-446655440000",
  projectId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             | Example                                                                 |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `title`                                                                 | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |                                                                         |
| `clientId`                                                              | *string*                                                                | :heavy_check_mark:                                                      | UUID v4                                                                 | 550e8400-e29b-41d4-a716-446655440000                                    |
| `billingContactId`                                                      | *string*                                                                | :heavy_minus_sign:                                                      | UUID v4                                                                 | 550e8400-e29b-41d4-a716-446655440000                                    |
| `projectId`                                                             | *string*                                                                | :heavy_minus_sign:                                                      | UUID v4                                                                 | 550e8400-e29b-41d4-a716-446655440000                                    |
| `sendMode`                                                              | [models.ProposalCreateSendMode](../models/proposal-create-send-mode.md) | :heavy_minus_sign:                                                      | N/A                                                                     |                                                                         |
| `issueDate`                                                             | [Date](../types/rfcdate.md)                                             | :heavy_minus_sign:                                                      | N/A                                                                     |                                                                         |
| `expirationDate`                                                        | [Date](../types/rfcdate.md)                                             | :heavy_minus_sign:                                                      | N/A                                                                     |                                                                         |
| `eventDate`                                                             | [Date](../types/rfcdate.md)                                             | :heavy_minus_sign:                                                      | N/A                                                                     |                                                                         |
| `notes`                                                                 | *string*                                                                | :heavy_minus_sign:                                                      | N/A                                                                     |                                                                         |
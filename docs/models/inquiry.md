# Inquiry

## Example Usage

```typescript
import { Inquiry } from "@clientcasa/sdk/models";

let value: Inquiry = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  status: "received",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  contactId: "550e8400-e29b-41d4-a716-446655440000",
  submissionId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                               | Type                                                | Required                                            | Description                                         | Example                                             |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `id`                                                | *string*                                            | :heavy_check_mark:                                  | UUID v4                                             | 550e8400-e29b-41d4-a716-446655440000                |
| `status`                                            | [models.InquiryStatus](../models/inquiry-status.md) | :heavy_check_mark:                                  | N/A                                                 |                                                     |
| `clientId`                                          | *string*                                            | :heavy_check_mark:                                  | UUID v4                                             | 550e8400-e29b-41d4-a716-446655440000                |
| `contactId`                                         | *string*                                            | :heavy_check_mark:                                  | UUID v4                                             | 550e8400-e29b-41d4-a716-446655440000                |
| `submissionId`                                      | *string*                                            | :heavy_check_mark:                                  | UUID v4                                             | 550e8400-e29b-41d4-a716-446655440000                |
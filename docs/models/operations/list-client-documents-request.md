# ListClientDocumentsRequest

## Example Usage

```typescript
import { ListClientDocumentsRequest } from "@clientcasa/sdk/models/operations";

let value: ListClientDocumentsRequest = {
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  contactId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     | Example                                                                                         |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `page`                                                                                          | *number*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |                                                                                                 |
| `pageSize`                                                                                      | *number*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |                                                                                                 |
| `status`                                                                                        | [operations.ListClientDocumentsStatus](../../models/operations/list-client-documents-status.md) | :heavy_minus_sign:                                                                              | N/A                                                                                             |                                                                                                 |
| `clientId`                                                                                      | *string*                                                                                        | :heavy_minus_sign:                                                                              | UUID v4                                                                                         | 550e8400-e29b-41d4-a716-446655440000                                                            |
| `contactId`                                                                                     | *string*                                                                                        | :heavy_minus_sign:                                                                              | UUID v4                                                                                         | 550e8400-e29b-41d4-a716-446655440000                                                            |
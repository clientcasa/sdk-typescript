# ListDocumentVersionsRequest

## Example Usage

```typescript
import { ListDocumentVersionsRequest } from "@clientcasa/sdk/models/operations";

let value: ListDocumentVersionsRequest = {
  documentId: "550e8400-e29b-41d4-a716-446655440000",
  invoiceId: "550e8400-e29b-41d4-a716-446655440000",
  contractId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `page`                                                              | *number*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |                                                                     |
| `pageSize`                                                          | *number*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |                                                                     |
| `documentType`                                                      | [operations.DocumentType](../../models/operations/document-type.md) | :heavy_minus_sign:                                                  | N/A                                                                 |                                                                     |
| `documentId`                                                        | *string*                                                            | :heavy_minus_sign:                                                  | Filter to a smart-file (client-document) id.                        | 550e8400-e29b-41d4-a716-446655440000                                |
| `invoiceId`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | Filter to an invoice id.                                            | 550e8400-e29b-41d4-a716-446655440000                                |
| `contractId`                                                        | *string*                                                            | :heavy_minus_sign:                                                  | Filter to a standalone-contract id.                                 | 550e8400-e29b-41d4-a716-446655440000                                |
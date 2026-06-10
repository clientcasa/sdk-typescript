# ListFormSubmissionsRequest

## Example Usage

```typescript
import { ListFormSubmissionsRequest } from "@clientcasa/sdk/models/operations";

let value: ListFormSubmissionsRequest = {
  formId: "550e8400-e29b-41d4-a716-446655440000",
  contactId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     | Example                                                                                         |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `page`                                                                                          | *number*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |                                                                                                 |
| `pageSize`                                                                                      | *number*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |                                                                                                 |
| `formId`                                                                                        | *string*                                                                                        | :heavy_minus_sign:                                                                              | UUID v4                                                                                         | 550e8400-e29b-41d4-a716-446655440000                                                            |
| `kind`                                                                                          | [operations.ListFormSubmissionsKind](../../models/operations/list-form-submissions-kind.md)     | :heavy_minus_sign:                                                                              | N/A                                                                                             |                                                                                                 |
| `status`                                                                                        | [operations.ListFormSubmissionsStatus](../../models/operations/list-form-submissions-status.md) | :heavy_minus_sign:                                                                              | N/A                                                                                             |                                                                                                 |
| `contactId`                                                                                     | *string*                                                                                        | :heavy_minus_sign:                                                                              | UUID v4                                                                                         | 550e8400-e29b-41d4-a716-446655440000                                                            |
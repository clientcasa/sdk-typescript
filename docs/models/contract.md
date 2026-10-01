# Contract

## Example Usage

```typescript
import { Contract } from "@clientcasa/sdk/models";

let value: Contract = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  contractNumber: "<value>",
  title: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  billingContactId: "550e8400-e29b-41d4-a716-446655440000",
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  sourceTemplateId: "550e8400-e29b-41d4-a716-446655440000",
  status: "voided",
  contentType: "tiptap",
  issueDate: new Date("2025-02-11"),
  effectiveDate: new Date("2025-08-16"),
  expirationDate: new Date("2024-08-30"),
  signedDate: new Date("2024-09-06T19:00:57.168Z"),
  currency: "Uganda Shilling",
  contractValue: 5068.39,
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
  archived: true,
  archivedAt: new Date("2026-12-07T18:15:53.435Z"),
  createdAt: new Date("2024-02-24T21:20:38.669Z"),
  updatedAt: new Date("2026-02-02T08:21:47.241Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `contractNumber`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `clientId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `billingContactId`                                                                            | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `projectId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `sourceTemplateId`                                                                            | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `status`                                                                                      | [models.ContractStatus](../models/contract-status.md)                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `contentType`                                                                                 | [models.ContentType](../models/content-type.md)                                               | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `issueDate`                                                                                   | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `effectiveDate`                                                                               | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `expirationDate`                                                                              | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `signedDate`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `contractValue`                                                                               | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `signers`                                                                                     | [models.Signer](../models/signer.md)[]                                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `archived`                                                                                    | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `archivedAt`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
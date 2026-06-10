# FormSubmission

## Example Usage

```typescript
import { FormSubmission } from "@clientcasa/sdk/models";

let value: FormSubmission = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  formId: "550e8400-e29b-41d4-a716-446655440000",
  kind: "inquiry",
  status: "in_progress",
  contactId: "550e8400-e29b-41d4-a716-446655440000",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  source: "<value>",
  submittedAt: new Date("2025-12-03"),
  answers: [
    {
      fieldId: "<id>",
      question: "<value>",
      answer: "<value>",
    },
  ],
  createdAt: new Date("2026-03-19T01:47:11.788Z"),
  updatedAt: new Date("2025-07-11T12:19:35.086Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `formId`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `kind`                                                                                        | [models.FormSubmissionKind](../models/form-submission-kind.md)                                | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `status`                                                                                      | [models.FormSubmissionStatus](../models/form-submission-status.md)                            | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `contactId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `clientId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `source`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `submittedAt`                                                                                 | [Date](../types/rfcdate.md)                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `answers`                                                                                     | [models.FormSubmissionAnswer](../models/form-submission-answer.md)[]                          | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
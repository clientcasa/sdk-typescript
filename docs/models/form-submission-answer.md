# FormSubmissionAnswer

## Example Usage

```typescript
import { FormSubmissionAnswer } from "@clientcasa/sdk/models";

let value: FormSubmissionAnswer = {
  fieldId: "<id>",
  question: "<value>",
  answer: "<value>",
  attachments: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      filename: "example.file",
      mimeType: "<value>",
      filesize: 343690,
    },
  ],
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `fieldId`                                                                    | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `question`                                                                   | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `answer`                                                                     | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `attachments`                                                                | [models.FormSubmissionAttachment](../models/form-submission-attachment.md)[] | :heavy_minus_sign:                                                           | N/A                                                                          |
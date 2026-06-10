# FormSubmissionList

## Example Usage

```typescript
import { FormSubmissionList } from "@clientcasa/sdk/models";

let value: FormSubmissionList = {
  data: [
    {
      id: "550e8400-e29b-41d4-a716-446655440000",
      formId: "550e8400-e29b-41d4-a716-446655440000",
      kind: "inquiry",
      status: "submitted",
      contactId: "550e8400-e29b-41d4-a716-446655440000",
      clientId: "550e8400-e29b-41d4-a716-446655440000",
      source: "<value>",
      submittedAt: new Date("2026-04-06"),
      answers: [
        {
          fieldId: "<id>",
          question: "<value>",
          answer: "<value>",
        },
      ],
      createdAt: new Date("2024-05-31T19:29:23.428Z"),
      updatedAt: new Date("2026-06-02T01:10:46.074Z"),
    },
  ],
  pagination: {
    page: 299018,
    pageSize: 331897,
    total: 615983,
    totalPages: 226919,
    hasMore: true,
  },
};
```

## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `data`                                                  | [models.FormSubmission](../models/form-submission.md)[] | :heavy_check_mark:                                      | N/A                                                     |
| `pagination`                                            | [models.PaginationMeta](../models/pagination-meta.md)   | :heavy_check_mark:                                      | N/A                                                     |
# RecordProjectActRequestBody

## Example Usage

```typescript
import { RecordProjectActRequestBody } from "@clientcasa/sdk/models/operations";

let value: RecordProjectActRequestBody = {
  commandId: "fc675439-996b-49ed-beb0-5fc6ed34719c",
  expectedRevision: 469582,
  intent: "resume",
  evidence: {
    precision: "day",
    occurredOn: "<value>",
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `commandId`                                                                               | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `expectedRevision`                                                                        | *number*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `intent`                                                                                  | [operations.RecordProjectActIntent](../../models/operations/record-project-act-intent.md) | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `evidence`                                                                                | *operations.Evidence*                                                                     | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `note`                                                                                    | *string*                                                                                  | :heavy_minus_sign:                                                                        | N/A                                                                                       |
| `evidenceLink`                                                                            | *string*                                                                                  | :heavy_minus_sign:                                                                        | N/A                                                                                       |
| `correctsEventId`                                                                         | *string*                                                                                  | :heavy_minus_sign:                                                                        | N/A                                                                                       |
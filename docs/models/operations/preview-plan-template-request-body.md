# PreviewPlanTemplateRequestBody

## Example Usage

```typescript
import { PreviewPlanTemplateRequestBody } from "@clientcasa/sdk/models/operations";

let value: PreviewPlanTemplateRequestBody = {
  templateId: "<id>",
  projectId: "488e9a0e-53d2-4135-88ca-a6fa8484ab3b",
  commandId: "718a4bb1-509b-4cc0-9456-0f448a2ba0d5",
};
```

## Fields

| Field                    | Type                     | Required                 | Description              |
| ------------------------ | ------------------------ | ------------------------ | ------------------------ |
| `templateId`             | *string*                 | :heavy_check_mark:       | N/A                      |
| `projectId`              | *string*                 | :heavy_check_mark:       | N/A                      |
| `anchors`                | Record<string, *string*> | :heavy_minus_sign:       | N/A                      |
| `withoutDates`           | *boolean*                | :heavy_minus_sign:       | N/A                      |
| `commandId`              | *string*                 | :heavy_check_mark:       | N/A                      |
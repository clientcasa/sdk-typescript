# FormAttachmentDownload

## Example Usage

```typescript
import { FormAttachmentDownload } from "@clientcasa/sdk/models";

let value: FormAttachmentDownload = {
  id: "550e8400-e29b-41d4-a716-446655440000",
  filename: "example.file",
  mimeType: "<value>",
  filesize: 412167,
  downloadUrl: "https://crafty-forage.net/",
  expiresAt: new Date("2025-07-21T17:54:44.097Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | UUID v4                                                                                       | 550e8400-e29b-41d4-a716-446655440000                                                          |
| `filename`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `mimeType`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `filesize`                                                                                    | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `downloadUrl`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |                                                                                               |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp (UTC)                                                                      |                                                                                               |
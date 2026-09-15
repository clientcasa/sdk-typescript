# FormAttachments

## Overview

### Available Operations

* [get](#get) - Get a form attachment download link

## get

Returns the attachment metadata plus a short-lived direct download link. The link expires — fetch it promptly and do not store it; request the attachment again for a fresh one. The scope is `form-submissions:read`: an attachment belongs to a submission, so a token that may read submissions may read their files. The link always downloads rather than renders inline, because these bytes were uploaded by an anonymous visitor through a public form.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getFormAttachment" method="get" path="/api/v1/form-attachments/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.formAttachments.get({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { formAttachmentsGet } from "@clientcasa/sdk/funcs/form-attachments-get.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await formAttachmentsGet(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("formAttachmentsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetFormAttachmentRequest](../../models/operations/get-form-attachment-request.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.GetFormAttachmentSecurity](../../models/operations/get-form-attachment-security.md)                                                                                | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.FormAttachmentDownload](../../models/form-attachment-download.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 401, 403, 404, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |
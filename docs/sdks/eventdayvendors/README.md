# EventDayVendors

## Overview

### Available Operations

* [list](#list) - List event day vendors
* [create](#create) - Add a vendor to an event day
* [get](#get) - Get an event day vendor
* [delete](#delete) - Remove a vendor from an event day
* [update](#update) - Update an event day vendor

## list

List event day vendors

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listEventDayVendors" method="get" path="/api/v1/event-day-vendors" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.eventDayVendors.list({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  for await (const page of result) {
    console.log(page);
  }
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { eventDayVendorsList } from "@clientcasa/sdk/funcs/event-day-vendors-list.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await eventDayVendorsList(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("eventDayVendorsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListEventDayVendorsRequest](../../models/operations/list-event-day-vendors-request.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ListEventDayVendorsSecurity](../../models/operations/list-event-day-vendors-security.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListEventDayVendorsResponse](../../models/operations/list-event-day-vendors-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## create

Add a vendor to an event day

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createEventDayVendor" method="post" path="/api/v1/event-day-vendors" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.eventDayVendors.create({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      eventDayId: "<id>",
      vendorId: "<id>",
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { eventDayVendorsCreate } from "@clientcasa/sdk/funcs/event-day-vendors-create.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await eventDayVendorsCreate(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      eventDayId: "<id>",
      vendorId: "<id>",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("eventDayVendorsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateEventDayVendorRequest](../../models/operations/create-event-day-vendor-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.CreateEventDayVendorSecurity](../../models/operations/create-event-day-vendor-security.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.EventDayVendor](../../models/event-day-vendor.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 409, 429       | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## get

Get an event day vendor

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getEventDayVendor" method="get" path="/api/v1/event-day-vendors/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.eventDayVendors.get({
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
import { eventDayVendorsGet } from "@clientcasa/sdk/funcs/event-day-vendors-get.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await eventDayVendorsGet(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("eventDayVendorsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetEventDayVendorRequest](../../models/operations/get-event-day-vendor-request.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.GetEventDayVendorSecurity](../../models/operations/get-event-day-vendor-security.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.EventDayVendor](../../models/event-day-vendor.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 401, 403, 404, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## delete

Remove a vendor from an event day

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteEventDayVendor" method="delete" path="/api/v1/event-day-vendors/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  await clientCasa.eventDayVendors.delete({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { eventDayVendorsDelete } from "@clientcasa/sdk/funcs/event-day-vendors-delete.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await eventDayVendorsDelete(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("eventDayVendorsDelete failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteEventDayVendorRequest](../../models/operations/delete-event-day-vendor-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.DeleteEventDayVendorSecurity](../../models/operations/delete-event-day-vendor-security.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 401, 403, 404, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## update

Update an event day vendor

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateEventDayVendor" method="patch" path="/api/v1/event-day-vendors/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.eventDayVendors.update({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    body: {},
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { eventDayVendorsUpdate } from "@clientcasa/sdk/funcs/event-day-vendors-update.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await eventDayVendorsUpdate(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("eventDayVendorsUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateEventDayVendorRequest](../../models/operations/update-event-day-vendor-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.UpdateEventDayVendorSecurity](../../models/operations/update-event-day-vendor-security.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.EventDayVendor](../../models/event-day-vendor.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 429       | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |
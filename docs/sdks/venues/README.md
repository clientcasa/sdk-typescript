# Venues

## Overview

### Available Operations

* [list](#list) - List venues
* [create](#create) - Create a venue
* [get](#get) - Get a venue
* [delete](#delete) - Delete a venue
* [update](#update) - Update a venue

## list

List venues

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listVenues" method="get" path="/api/v1/venues" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.venues.list({
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
import { venuesList } from "@clientcasa/sdk/funcs/venues-list.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await venuesList(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("venuesList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListVenuesRequest](../../models/operations/list-venues-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ListVenuesSecurity](../../models/operations/list-venues-security.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListVenuesResponse](../../models/operations/list-venues-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## create

Create a venue

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createVenue" method="post" path="/api/v1/venues" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.venues.create({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      name: "<value>",
      tagIds: [
        "550e8400-e29b-41d4-a716-446655440000",
      ],
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
import { venuesCreate } from "@clientcasa/sdk/funcs/venues-create.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await venuesCreate(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      name: "<value>",
      tagIds: [
        "550e8400-e29b-41d4-a716-446655440000",
      ],
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("venuesCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateVenueRequest](../../models/operations/create-venue-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.CreateVenueSecurity](../../models/operations/create-venue-security.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Venue](../../models/venue.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 409, 429       | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## get

Get a venue

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getVenue" method="get" path="/api/v1/venues/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.venues.get({
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
import { venuesGet } from "@clientcasa/sdk/funcs/venues-get.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await venuesGet(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("venuesGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetVenueRequest](../../models/operations/get-venue-request.md)                                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.GetVenueSecurity](../../models/operations/get-venue-security.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Venue](../../models/venue.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 401, 403, 404, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## delete

Delete a venue

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteVenue" method="delete" path="/api/v1/venues/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  await clientCasa.venues.delete({
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
import { venuesDelete } from "@clientcasa/sdk/funcs/venues-delete.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await venuesDelete(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("venuesDelete failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteVenueRequest](../../models/operations/delete-venue-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.DeleteVenueSecurity](../../models/operations/delete-venue-security.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
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

Update a venue

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateVenue" method="patch" path="/api/v1/venues/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.venues.update({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    body: {
      tagIds: [
        "550e8400-e29b-41d4-a716-446655440000",
      ],
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
import { venuesUpdate } from "@clientcasa/sdk/funcs/venues-update.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await venuesUpdate(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    body: {
      tagIds: [
        "550e8400-e29b-41d4-a716-446655440000",
      ],
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("venuesUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateVenueRequest](../../models/operations/update-venue-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.UpdateVenueSecurity](../../models/operations/update-venue-security.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Venue](../../models/venue.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 429       | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |
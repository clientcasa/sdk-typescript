# Milestones

## Overview

### Available Operations

* [listMilestones](#listmilestones) - List milestones
* [createMilestone](#createmilestone) - Create a milestone
* [getMilestone](#getmilestone) - Get a milestone
* [deleteMilestone](#deletemilestone) - Delete a milestone
* [updateMilestone](#updatemilestone) - Update a milestone

## listMilestones

List milestones

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listMilestones" method="get" path="/api/v1/milestones" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.milestones.listMilestones({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    parentId: "550e8400-e29b-41d4-a716-446655440000",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { milestonesListMilestones } from "@clientcasa/sdk/funcs/milestones-list-milestones.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await milestonesListMilestones(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    parentId: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("milestonesListMilestones failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListMilestonesRequest](../../models/operations/list-milestones-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ListMilestonesSecurity](../../models/operations/list-milestones-security.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListMilestonesResponse](../../models/operations/list-milestones-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## createMilestone

Milestones attach to either a project or a proposal — `parentType` + `parentId` are both required.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createMilestone" method="post" path="/api/v1/milestones" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.milestones.createMilestone({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    parentType: "proposals",
    parentId: "550e8400-e29b-41d4-a716-446655440000",
    title: "<value>",
    date: new Date("2025-07-24"),
    assigneeId: "550e8400-e29b-41d4-a716-446655440000",
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { milestonesCreateMilestone } from "@clientcasa/sdk/funcs/milestones-create-milestone.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await milestonesCreateMilestone(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    parentType: "proposals",
    parentId: "550e8400-e29b-41d4-a716-446655440000",
    title: "<value>",
    date: new Date("2025-07-24"),
    assigneeId: "550e8400-e29b-41d4-a716-446655440000",
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("milestonesCreateMilestone failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.MilestoneCreate](../../models/milestone-create.md)                                                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.CreateMilestoneSecurity](../../models/operations/create-milestone-security.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Milestone](../../models/milestone.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## getMilestone

Get a milestone

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getMilestone" method="get" path="/api/v1/milestones/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.milestones.getMilestone({
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
import { milestonesGetMilestone } from "@clientcasa/sdk/funcs/milestones-get-milestone.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await milestonesGetMilestone(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("milestonesGetMilestone failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetMilestoneRequest](../../models/operations/get-milestone-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.GetMilestoneSecurity](../../models/operations/get-milestone-security.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Milestone](../../models/milestone.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## deleteMilestone

Delete a milestone

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteMilestone" method="delete" path="/api/v1/milestones/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  await clientCasa.milestones.deleteMilestone({
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
import { milestonesDeleteMilestone } from "@clientcasa/sdk/funcs/milestones-delete-milestone.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await milestonesDeleteMilestone(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("milestonesDeleteMilestone failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteMilestoneRequest](../../models/operations/delete-milestone-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.DeleteMilestoneSecurity](../../models/operations/delete-milestone-security.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## updateMilestone

Update a milestone

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateMilestone" method="patch" path="/api/v1/milestones/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.milestones.updateMilestone({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    body: {
      assigneeId: "550e8400-e29b-41d4-a716-446655440000",
      catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
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
import { milestonesUpdateMilestone } from "@clientcasa/sdk/funcs/milestones-update-milestone.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await milestonesUpdateMilestone(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    body: {
      assigneeId: "550e8400-e29b-41d4-a716-446655440000",
      catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("milestonesUpdateMilestone failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateMilestoneRequest](../../models/operations/update-milestone-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.UpdateMilestoneSecurity](../../models/operations/update-milestone-security.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Milestone](../../models/milestone.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |
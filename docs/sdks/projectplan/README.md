# ProjectPlan

## Overview

### Available Operations

* [startTodo](#starttodo) - start Todo
* [completeTodo](#completetodo) - complete Todo
* [reopenTodo](#reopentodo) - reopen Todo
* [cancelTodo](#canceltodo) - cancel Todo
* [restoreTodo](#restoretodo) - restore Todo
* [changeTodoOccurrence](#changetodooccurrence) - change Todo Occurrence
* [list](#list) - Read a project plan
* [previewPlanTemplate](#previewplantemplate) - preview Plan Template
* [applyPlanTemplate](#applyplantemplate) - apply Plan Template
* [previewPlanDateChange](#previewplandatechange) - preview Plan Date Change
* [applyPlanDateChange](#applyplandatechange) - apply Plan Date Change
* [recordProjectAct](#recordprojectact) - record Project Act
* [listEvents](#listevents) - Sample actual announced plan events

## startTodo

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="startTodo" method="post" path="/api/v1/to-dos/{id}/start" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.startTodo({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 266187,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
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
import { projectPlanStartTodo } from "@clientcasa/sdk/funcs/project-plan-start-todo.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanStartTodo(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 266187,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanStartTodo failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.StartTodoRequest](../../models/operations/start-todo-request.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.StartTodoSecurity](../../models/operations/start-todo-security.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.TodoCommandResult](../../models/todo-command-result.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## completeTodo

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="completeTodo" method="post" path="/api/v1/to-dos/{id}/complete" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.completeTodo({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 593867,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
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
import { projectPlanCompleteTodo } from "@clientcasa/sdk/funcs/project-plan-complete-todo.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanCompleteTodo(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 593867,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanCompleteTodo failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CompleteTodoRequest](../../models/operations/complete-todo-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.CompleteTodoSecurity](../../models/operations/complete-todo-security.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.TodoCommandResult](../../models/todo-command-result.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## reopenTodo

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="reopenTodo" method="post" path="/api/v1/to-dos/{id}/reopen" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.reopenTodo({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 67813,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
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
import { projectPlanReopenTodo } from "@clientcasa/sdk/funcs/project-plan-reopen-todo.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanReopenTodo(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 67813,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanReopenTodo failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ReopenTodoRequest](../../models/operations/reopen-todo-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ReopenTodoSecurity](../../models/operations/reopen-todo-security.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.TodoCommandResult](../../models/todo-command-result.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## cancelTodo

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="cancelTodo" method="post" path="/api/v1/to-dos/{id}/cancel" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.cancelTodo({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 54359,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
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
import { projectPlanCancelTodo } from "@clientcasa/sdk/funcs/project-plan-cancel-todo.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanCancelTodo(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 54359,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanCancelTodo failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CancelTodoRequest](../../models/operations/cancel-todo-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.CancelTodoSecurity](../../models/operations/cancel-todo-security.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.TodoCommandResult](../../models/todo-command-result.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## restoreTodo

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="restoreTodo" method="post" path="/api/v1/to-dos/{id}/restore" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.restoreTodo({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 712169,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
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
import { projectPlanRestoreTodo } from "@clientcasa/sdk/funcs/project-plan-restore-todo.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanRestoreTodo(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "550e8400-e29b-41d4-a716-446655440000",
      expectedRevision: 712169,
      billingReviewId: "550e8400-e29b-41d4-a716-446655440000",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanRestoreTodo failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.RestoreTodoRequest](../../models/operations/restore-todo-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.RestoreTodoSecurity](../../models/operations/restore-todo-security.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.TodoCommandResult](../../models/todo-command-result.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## changeTodoOccurrence

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="changeTodoOccurrence" method="post" path="/api/v1/to-dos/occurrences" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.changeTodoOccurrence({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      intent: "occurrence",
      commandId: "1bbefaa6-6f12-4366-85d8-e3c90791de0c",
      seriesId: "388ccc04-35c3-491f-a0fd-34ea23da951a",
      nominalKey: "<value>",
      expectedRevision: 726720,
      todoId: "de58424d-2981-4391-b4ff-4b0f2e0d329d",
      action: "edit",
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
import { projectPlanChangeTodoOccurrence } from "@clientcasa/sdk/funcs/project-plan-change-todo-occurrence.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanChangeTodoOccurrence(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      intent: "occurrence",
      commandId: "1bbefaa6-6f12-4366-85d8-e3c90791de0c",
      seriesId: "388ccc04-35c3-491f-a0fd-34ea23da951a",
      nominalKey: "<value>",
      expectedRevision: 726720,
      todoId: "de58424d-2981-4391-b4ff-4b0f2e0d329d",
      action: "edit",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanChangeTodoOccurrence failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ChangeTodoOccurrenceRequest](../../models/operations/change-todo-occurrence-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ChangeTodoOccurrenceSecurity](../../models/operations/change-todo-occurrence-security.md)                                                                          | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## list

Read a project plan

### Example Usage

<!-- UsageSnippet language="typescript" operationID="readPlan" method="get" path="/api/v1/plans" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.list({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    projectId: "550e8400-e29b-41d4-a716-446655440000",
    clientId: "550e8400-e29b-41d4-a716-446655440000",
    eventDayId: "550e8400-e29b-41d4-a716-446655440000",
  });

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
import { projectPlanList } from "@clientcasa/sdk/funcs/project-plan-list.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanList(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    projectId: "550e8400-e29b-41d4-a716-446655440000",
    clientId: "550e8400-e29b-41d4-a716-446655440000",
    eventDayId: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("projectPlanList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ReadPlanRequest](../../models/operations/read-plan-request.md)                                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ReadPlanSecurity](../../models/operations/read-plan-security.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ReadPlanResponse](../../models/operations/read-plan-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## previewPlanTemplate

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="previewPlanTemplate" method="post" path="/api/v1/plans/templates/preview" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.previewPlanTemplate({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      templateId: "<id>",
      projectId: "df112acd-3647-4d99-8f06-268c6637ffda",
      commandId: "bb4774d4-208e-468b-b171-9f0221c59183",
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
import { projectPlanPreviewPlanTemplate } from "@clientcasa/sdk/funcs/project-plan-preview-plan-template.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanPreviewPlanTemplate(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      templateId: "<id>",
      projectId: "df112acd-3647-4d99-8f06-268c6637ffda",
      commandId: "bb4774d4-208e-468b-b171-9f0221c59183",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanPreviewPlanTemplate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PreviewPlanTemplateRequest](../../models/operations/preview-plan-template-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.PreviewPlanTemplateSecurity](../../models/operations/preview-plan-template-security.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## applyPlanTemplate

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="applyPlanTemplate" method="post" path="/api/v1/plans/templates/apply" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.applyPlanTemplate({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "6840335a-aea6-4ada-beef-999e950d8a80",
      previewId: "3c6b56d8-ace6-4616-b792-c253219f117b",
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
import { projectPlanApplyPlanTemplate } from "@clientcasa/sdk/funcs/project-plan-apply-plan-template.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanApplyPlanTemplate(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "6840335a-aea6-4ada-beef-999e950d8a80",
      previewId: "3c6b56d8-ace6-4616-b792-c253219f117b",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanApplyPlanTemplate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ApplyPlanTemplateRequest](../../models/operations/apply-plan-template-request.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ApplyPlanTemplateSecurity](../../models/operations/apply-plan-template-security.md)                                                                                | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## previewPlanDateChange

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="previewPlanDateChange" method="post" path="/api/v1/plans/dates/preview" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.previewPlanDateChange({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "3f6bfda7-b750-468b-908b-ee4094b32f12",
      projectId: "0f32c6e9-4ccf-4351-a9d1-c1885a1ba3b1",
      day: new Date("2025-02-13"),
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
import { projectPlanPreviewPlanDateChange } from "@clientcasa/sdk/funcs/project-plan-preview-plan-date-change.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanPreviewPlanDateChange(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "3f6bfda7-b750-468b-908b-ee4094b32f12",
      projectId: "0f32c6e9-4ccf-4351-a9d1-c1885a1ba3b1",
      day: new Date("2025-02-13"),
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanPreviewPlanDateChange failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PreviewPlanDateChangeRequest](../../models/operations/preview-plan-date-change-request.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.PreviewPlanDateChangeSecurity](../../models/operations/preview-plan-date-change-security.md)                                                                       | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## applyPlanDateChange

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="applyPlanDateChange" method="post" path="/api/v1/plans/dates/apply" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.applyPlanDateChange({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "2a6c8f95-4d61-4e0f-a70e-f504451878b0",
      previewId: "91588094-4f47-4390-939c-550b096437d5",
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
import { projectPlanApplyPlanDateChange } from "@clientcasa/sdk/funcs/project-plan-apply-plan-date-change.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanApplyPlanDateChange(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "2a6c8f95-4d61-4e0f-a70e-f504451878b0",
      previewId: "91588094-4f47-4390-939c-550b096437d5",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanApplyPlanDateChange failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ApplyPlanDateChangeRequest](../../models/operations/apply-plan-date-change-request.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ApplyPlanDateChangeSecurity](../../models/operations/apply-plan-date-change-security.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## recordProjectAct

Requires write:to-dos, stable commandId and current rights. Billed completion requires an actor-bound reviewed billingReviewId; otherwise plan_billing_review_required. Event-date and template changes require an exact current preview receipt. No command records payment or sends a client message.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="recordProjectAct" method="post" path="/api/v1/projects/{id}/acts" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.recordProjectAct({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "2b435607-2063-4d46-afaf-aa746a47820f",
      expectedRevision: 488954,
      intent: "cancel",
      evidence: {
        precision: "instant",
        occurredAt: new Date("2026-06-11T15:33:15.198Z"),
      },
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
import { projectPlanRecordProjectAct } from "@clientcasa/sdk/funcs/project-plan-record-project-act.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanRecordProjectAct(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    idempotencyKey: "create-client-2026-05-24-a1b2c3",
    body: {
      commandId: "2b435607-2063-4d46-afaf-aa746a47820f",
      expectedRevision: 488954,
      intent: "cancel",
      evidence: {
        precision: "instant",
        occurredAt: new Date("2026-06-11T15:33:15.198Z"),
      },
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanRecordProjectAct failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.RecordProjectActRequest](../../models/operations/record-project-act-request.md)                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.RecordProjectActSecurity](../../models/operations/record-project-act-security.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 404, 409, 429  | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## listEvents

Sample actual announced plan events

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listPlanEvents" method="get" path="/api/v1/plan-events" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.projectPlan.listEvents({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    event: "todo_completed",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { projectPlanListEvents } from "@clientcasa/sdk/funcs/project-plan-list-events.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await projectPlanListEvents(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    event: "todo_completed",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("projectPlanListEvents failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListPlanEventsRequest](../../models/operations/list-plan-events-request.md)                                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ListPlanEventsSecurity](../../models/operations/list-plan-events-security.md)                                                                                      | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PlanEventSamples](../../models/plan-event-samples.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ApiError               | 400, 401, 403, 429            | application/json              |
| errors.ApiError               | 500                           | application/json              |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |
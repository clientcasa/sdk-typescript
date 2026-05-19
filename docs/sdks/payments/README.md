# Payments

## Overview

### Available Operations

* [listPayments](#listpayments) - List payments
* [createPayment](#createpayment) - Record a manual payment
* [getPayment](#getpayment) - Get a payment
* [updatePayment](#updatepayment) - Update a payment (notes/reference only — payments are otherwise immutable)

## listPayments

List payments

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listPayments" method="get" path="/api/v1/payments" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.payments.listPayments({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    clientId: "550e8400-e29b-41d4-a716-446655440000",
    invoiceId: "550e8400-e29b-41d4-a716-446655440000",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { paymentsListPayments } from "@clientcasa/sdk/funcs/payments-list-payments.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await paymentsListPayments(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    clientId: "550e8400-e29b-41d4-a716-446655440000",
    invoiceId: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentsListPayments failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListPaymentsRequest](../../models/operations/list-payments-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.ListPaymentsSecurity](../../models/operations/list-payments-security.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListPaymentsResponse](../../models/operations/list-payments-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## createPayment

Records a manually-collected payment (check, bank transfer, cash, etc.). Stripe payments are recorded automatically via webhooks and cannot be created here. Payments are immutable after creation except for `reference` and `notes`. To reverse a payment, record a refund (kind=refund, negative amount, refundOfId pointing at the original).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createPayment" method="post" path="/api/v1/payments" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.payments.createPayment({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    clientId: "550e8400-e29b-41d4-a716-446655440000",
    invoiceId: "550e8400-e29b-41d4-a716-446655440000",
    amount: 8834.59,
    receivedDate: new Date("2026-11-18"),
    method: "zelle",
    refundOfId: "550e8400-e29b-41d4-a716-446655440000",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ClientCasaCore } from "@clientcasa/sdk/core.js";
import { paymentsCreatePayment } from "@clientcasa/sdk/funcs/payments-create-payment.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await paymentsCreatePayment(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    clientId: "550e8400-e29b-41d4-a716-446655440000",
    invoiceId: "550e8400-e29b-41d4-a716-446655440000",
    amount: 8834.59,
    receivedDate: new Date("2026-11-18"),
    method: "zelle",
    refundOfId: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentsCreatePayment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.PaymentCreate](../../models/payment-create.md)                                                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.CreatePaymentSecurity](../../models/operations/create-payment-security.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Payment](../../models/payment.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## getPayment

Get a payment

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getPayment" method="get" path="/api/v1/payments/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.payments.getPayment({
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
import { paymentsGetPayment } from "@clientcasa/sdk/funcs/payments-get-payment.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await paymentsGetPayment(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentsGetPayment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetPaymentRequest](../../models/operations/get-payment-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.GetPaymentSecurity](../../models/operations/get-payment-security.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Payment](../../models/payment.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |

## updatePayment

Update a payment (notes/reference only — payments are otherwise immutable)

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updatePayment" method="patch" path="/api/v1/payments/{id}" -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.payments.updatePayment({
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
import { paymentsUpdatePayment } from "@clientcasa/sdk/funcs/payments-update-payment.js";

// Use `ClientCasaCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const clientCasa = new ClientCasaCore();

async function run() {
  const res = await paymentsUpdatePayment(clientCasa, {
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {
    id: "550e8400-e29b-41d4-a716-446655440000",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("paymentsUpdatePayment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdatePaymentRequest](../../models/operations/update-payment-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `security`                                                                                                                                                                     | [operations.UpdatePaymentSecurity](../../models/operations/update-payment-security.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The security requirements to use for the request.                                                                                                                              |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Payment](../../models/payment.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ClientCasaDefaultError | 4XX, 5XX                      | \*/\*                         |
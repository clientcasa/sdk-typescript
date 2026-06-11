# @clientcasa/sdk

Official TypeScript SDK for the [ClientCasa](https://www.clientcasa.com) REST API.

```bash
npm install @clientcasa/sdk
# or
pnpm add @clientcasa/sdk
# or
yarn add @clientcasa/sdk
```

Works in Node.js 18+, modern browsers, Edge runtimes, Cloudflare Workers, and Deno.

## Quick start

Get an API key from **Settings → API Keys** in your dashboard, then:

```ts
import { ClientCasa } from '@clientcasa/sdk'

const cc = new ClientCasa()
const security = { apiKey: process.env.CLIENTCASA_API_KEY ?? '' }

// List clients
const result = await cc.clients.listClients(security, { pageSize: 25 })
for (const client of result.data) {
  console.log(client.name, client.status)
}

// Create a client
const created = await cc.clients.createClient(security, {
  name: 'Acme Inc.',
  status: 'active',
})

// Get one by ID
const fetched = await cc.clients.getClient(security, { id: created.id })

// Update
await cc.clients.updateClient(security, {
  id: created.id,
  clientUpdate: { notes: 'Updated via SDK' },
})

// Delete
await cc.clients.deleteClient(security, { id: created.id })
```

Errors are thrown — wrap calls in `try/catch` to handle them.

## OAuth (third-party apps)

If you're building a third-party app that acts on behalf of a user, use the access token from your OAuth flow:

```ts
const security = { bearer: 'eyJhbGc...' }  // from /api/auth/oauth2/token
const result = await cc.clients.listClients(security, {})
```

See the [OAuth Apps guide](https://www.clientcasa.com/docs/api/oauth-apps) for the full authorization-code-with-PKCE flow.

## Resources

The client exposes one accessor per v1 resource. Method names follow the verb-then-resource pattern (`listClients`, `createInvoice`, `getPayout`, etc.):

| Accessor | Methods | Notes |
|---|---|---|
| `cc.clients` | listClients, createClient, getClient, updateClient, deleteClient | |
| `cc.contacts` | listContacts, createContact, getContact, updateContact, deleteContact | |
| `cc.projects` | listProjects, createProject, getProject, updateProject, deleteProject | |
| `cc.invoices` | listInvoices, createInvoice, getInvoice, updateInvoice, deleteInvoice | Status is payment-derived; only `draft`, `sent`, `void` writable |
| `cc.proposals` | listProposals, createProposal, getProposal, updateProposal, deleteProposal | Tiptap content not editable via API |
| `cc.contracts` | listContracts, createContract, getContract, updateContract, deleteContract | Create makes drafts only; signing is dashboard-managed |
| `cc.payments` | listPayments, createPayment, getPayment, updatePayment | Immutable — no delete. Refunds are negative-amount entries with `kind=refund` |
| `cc.payouts` | listPayouts, getPayout | Read-only — Stripe-managed |
| `cc.timeEntries` | listTimeEntries, createTimeEntry, getTimeEntry, updateTimeEntry, deleteTimeEntry | |
| `cc.milestones` | listMilestones, createMilestone, getMilestone, updateMilestone, deleteMilestone | Polymorphic parent (`parentType: 'projects' \| 'proposals'`) |
| `cc.calendarEvents` | listCalendarEvents, createCalendarEvent, getCalendarEvent, updateCalendarEvent, deleteCalendarEvent | Externally-synced events are read-only |
| `cc.inquiries` | listInquiries, createInquiry, getInquiry, updateInquiry, deleteInquiry | Inquiries land in `status: 'new'`; `converted` set by the dashboard |
| `cc.transactions` | listTransactions, createTransaction, getTransaction, updateTransaction, deleteTransaction | |
| `cc.catalogItems` | listCatalogItems, createCatalogItem, getCatalogItem, updateCatalogItem, deleteCatalogItem | |
| `cc.webhooks` | listWebhooks, createWebhook, getWebhook, updateWebhook, deleteWebhook | Secret is write-only |

## Error handling

Methods throw typed errors on non-2xx responses. Each operation has its own named error class:

```ts
import { ClientCasa } from '@clientcasa/sdk'
import { APIError, HTTPClientErrors } from '@clientcasa/sdk/models/errors'

try {
  const result = await cc.clients.getClient(security, { id: 'bad-id' })
  console.log(result.name)
} catch (err) {
  if (err instanceof APIError) {
    console.error(err.statusCode)            // 404
    console.error(err.message)               // human-readable
    // Decoded error body if the response was JSON:
    // err.body has { error: { code, message, requestId, details? } }
  } else {
    throw err
  }
}
```

See [`docs/models/errors/`](./docs/models/errors) for per-operation error types.

## Idempotency

Pass an `Idempotency-Key` header on write operations to safely retry:

```ts
import { randomUUID } from 'node:crypto'

await cc.invoices.createInvoice(
  security,
  {
    clientId: 'cli_...',
    issueDate: '2026-05-19',
    dueDate: '2026-06-18',
    lineItems: [{ description: 'Consult', quantity: 1, unitPrice: 500, taxable: false }],
  },
  { headers: { 'Idempotency-Key': randomUUID() } },
)
```

The same key replayed within 24h returns the cached response. See the [Idempotency guide](https://www.clientcasa.com/docs/integrations/idempotent-writes) for the full pattern, including payments and refunds.

## Configuration

```ts
import { ClientCasa } from '@clientcasa/sdk'

new ClientCasa({
  // Optional default API key — applied to every method that takes `security`.
  // Per-call security still overrides if both are set.
  apiKey: process.env.CLIENTCASA_API_KEY ?? '',
  // Override the production base URL (e.g., for staging or test envs)
  serverURL: 'https://www.clientcasa.com',
  // Override the underlying HTTP client (e.g., to inject middleware)
  httpClient: undefined,
  // Custom retry config (defaults are already sensible)
  retryConfig: undefined,
  // Per-call timeout in milliseconds
  timeoutMs: 30_000,
})
```

## TypeScript

All DTOs are exported under the `@clientcasa/sdk/models` subpath:

```ts
import type { Client, InvoiceCreate, PaginationMeta } from '@clientcasa/sdk/models'
```

Per-operation request/response types live under `@clientcasa/sdk/models/operations`.

## Contributing

This SDK is auto-generated from the [ClientCasa OpenAPI spec](https://www.clientcasa.com/api/v1/openapi.json) by [Speakeasy](https://www.speakeasy.com). Most changes belong upstream in the API, not here.

- **Found a bug or want a feature?** [Open an issue](https://github.com/clientcasa/sdk-typescript/issues) — include the SDK version, what you tried, and the unexpected behavior.
- **Want to suggest an SDK-specific improvement** (ergonomics, retries, packaging)? Open an issue and we'll discuss before code.
- **Security issue?** See [SECURITY.md](./SECURITY.md). Do not file a public issue.

Pull requests touching `src/generated/` will be regenerated and overwritten — please don't edit generated code directly. See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full contributor guide.

## Versioning

The SDK follows the API's v1 contract. Breaking changes go in a major version bump; new resources and new optional fields are minor versions.

## License

MIT

<!-- Start Summary [summary] -->
## Summary

ClientCasa API: REST API for ClientCasa — proposals, contracts, time tracking, expenses, invoicing, payments, and CRM for solo operators and small teams.
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [@clientcasa/sdk](#clientcasasdk)
  * [Quick start](#quick-start)
  * [OAuth (third-party apps)](#oauth-third-party-apps)
  * [Resources](#resources)
  * [Error handling](#error-handling)
  * [Idempotency](#idempotency)
  * [Configuration](#configuration)
  * [TypeScript](#typescript)
  * [Contributing](#contributing)
  * [Versioning](#versioning)
  * [License](#license)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Pagination](#pagination)
  * [Retries](#retries)
  * [Error Handling](#error-handling-1)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add @clientcasa/sdk
```

### PNPM

```bash
pnpm add @clientcasa/sdk
```

### Bun

```bash
bun add @clientcasa/sdk
```

### Yarn

```bash
yarn add @clientcasa/sdk
```

> [!NOTE]
> This package is published as an ES Module (ESM) only. For applications using
> CommonJS, use `await import("@clientcasa/sdk")` to import and use this package.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.clients.list({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name     | Type   | Scheme  | Environment Variable |
| -------- | ------ | ------- | -------------------- |
| `apiKey` | apiKey | API key | `CLIENTCASA_API_KEY` |

To authenticate with the API the `apiKey` parameter must be set when initializing the SDK client instance. For example:


### Per-Operation Security Schemes

Some operations in this SDK require the security scheme to be specified at the request level. For example:
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.clients.list({}, {});

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [CalendarEvents](docs/sdks/calendarevents/README.md)

* [list](docs/sdks/calendarevents/README.md#list) - List calendar events
* [create](docs/sdks/calendarevents/README.md#create) - Create a calendar event
* [get](docs/sdks/calendarevents/README.md#get) - Get a calendar event
* [delete](docs/sdks/calendarevents/README.md#delete) - Delete a calendar event
* [update](docs/sdks/calendarevents/README.md#update) - Update a calendar event

### [CatalogItems](docs/sdks/catalogitems/README.md)

* [list](docs/sdks/catalogitems/README.md#list) - List catalog items
* [create](docs/sdks/catalogitems/README.md#create) - Create a catalog item
* [get](docs/sdks/catalogitems/README.md#get) - Get a catalog item
* [delete](docs/sdks/catalogitems/README.md#delete) - Delete a catalog item
* [update](docs/sdks/catalogitems/README.md#update) - Update a catalog item

### [Clients](docs/sdks/clients/README.md)

* [list](docs/sdks/clients/README.md#list) - List clients
* [create](docs/sdks/clients/README.md#create) - Create a client
* [get](docs/sdks/clients/README.md#get) - Get a client
* [delete](docs/sdks/clients/README.md#delete) - Delete a client
* [update](docs/sdks/clients/README.md#update) - Update a client

### [Contacts](docs/sdks/contacts/README.md)

* [list](docs/sdks/contacts/README.md#list) - List contacts
* [create](docs/sdks/contacts/README.md#create) - Create a contact
* [get](docs/sdks/contacts/README.md#get) - Get a contact
* [delete](docs/sdks/contacts/README.md#delete) - Delete a contact
* [update](docs/sdks/contacts/README.md#update) - Update a contact

### [Contracts](docs/sdks/contracts/README.md)

* [list](docs/sdks/contracts/README.md#list) - List contracts
* [create](docs/sdks/contracts/README.md#create) - Create a draft contract
* [get](docs/sdks/contracts/README.md#get) - Get a contract
* [delete](docs/sdks/contracts/README.md#delete) - Delete a contract (only drafts)
* [update](docs/sdks/contracts/README.md#update) - Update a contract (limited fields)

### [DocumentVersions](docs/sdks/documentversions/README.md)

* [list](docs/sdks/documentversions/README.md#list) - List document versions
* [get](docs/sdks/documentversions/README.md#get) - Get a document version

### [FormSubmissions](docs/sdks/formsubmissions/README.md)

* [list](docs/sdks/formsubmissions/README.md#list) - List form submissions
* [get](docs/sdks/formsubmissions/README.md#get) - Get a form submission (with answers)

### [Forms](docs/sdks/forms/README.md)

* [list](docs/sdks/forms/README.md#list) - List forms
* [get](docs/sdks/forms/README.md#get) - Get a form

### [FormsAndAgreements](docs/sdks/formsandagreements/README.md)

* [list](docs/sdks/formsandagreements/README.md#list) - List proposals
* [get](docs/sdks/formsandagreements/README.md#get) - Get a proposal

### [Invoices](docs/sdks/invoices/README.md)

* [list](docs/sdks/invoices/README.md#list) - List invoices
* [create](docs/sdks/invoices/README.md#create) - Create an invoice
* [get](docs/sdks/invoices/README.md#get) - Get an invoice
* [delete](docs/sdks/invoices/README.md#delete) - Delete an invoice (only drafts)
* [update](docs/sdks/invoices/README.md#update) - Update an invoice (line items not editable in v1)

### [Milestones](docs/sdks/milestones/README.md)

* [list](docs/sdks/milestones/README.md#list) - List milestones
* [create](docs/sdks/milestones/README.md#create) - Create a milestone
* [get](docs/sdks/milestones/README.md#get) - Get a milestone
* [delete](docs/sdks/milestones/README.md#delete) - Delete a milestone
* [update](docs/sdks/milestones/README.md#update) - Update a milestone

### [Payments](docs/sdks/payments/README.md)

* [list](docs/sdks/payments/README.md#list) - List payments
* [create](docs/sdks/payments/README.md#create) - Record a manual payment
* [get](docs/sdks/payments/README.md#get) - Get a payment
* [update](docs/sdks/payments/README.md#update) - Update a payment (notes/reference only — payments are otherwise immutable)

### [Payouts](docs/sdks/payouts/README.md)

* [list](docs/sdks/payouts/README.md#list) - List payouts
* [get](docs/sdks/payouts/README.md#get) - Get a payout

### [Projects](docs/sdks/projects/README.md)

* [list](docs/sdks/projects/README.md#list) - List projects
* [create](docs/sdks/projects/README.md#create) - Create a project
* [get](docs/sdks/projects/README.md#get) - Get a project
* [delete](docs/sdks/projects/README.md#delete) - Delete a project
* [update](docs/sdks/projects/README.md#update) - Update a project

### [TimeEntries](docs/sdks/timeentries/README.md)

* [list](docs/sdks/timeentries/README.md#list) - List time entries
* [create](docs/sdks/timeentries/README.md#create) - Create a time entry
* [get](docs/sdks/timeentries/README.md#get) - Get a time entry
* [delete](docs/sdks/timeentries/README.md#delete) - Delete a time entry
* [update](docs/sdks/timeentries/README.md#update) - Update a time entry

### [Transactions](docs/sdks/transactions/README.md)

* [list](docs/sdks/transactions/README.md#list) - List transactions
* [create](docs/sdks/transactions/README.md#create) - Create a transaction (expense or charge)
* [get](docs/sdks/transactions/README.md#get) - Get a transaction
* [delete](docs/sdks/transactions/README.md#delete) - Delete a transaction
* [update](docs/sdks/transactions/README.md#update) - Update a transaction

### [Webhooks](docs/sdks/webhooks/README.md)

* [list](docs/sdks/webhooks/README.md#list) - List webhook subscriptions
* [create](docs/sdks/webhooks/README.md#create) - Subscribe to events
* [get](docs/sdks/webhooks/README.md#get) - Get a webhook
* [delete](docs/sdks/webhooks/README.md#delete) - Delete a webhook
* [update](docs/sdks/webhooks/README.md#update) - Update a webhook

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`calendarEventsCreate`](docs/sdks/calendarevents/README.md#create) - Create a calendar event
- [`calendarEventsDelete`](docs/sdks/calendarevents/README.md#delete) - Delete a calendar event
- [`calendarEventsGet`](docs/sdks/calendarevents/README.md#get) - Get a calendar event
- [`calendarEventsList`](docs/sdks/calendarevents/README.md#list) - List calendar events
- [`calendarEventsUpdate`](docs/sdks/calendarevents/README.md#update) - Update a calendar event
- [`catalogItemsCreate`](docs/sdks/catalogitems/README.md#create) - Create a catalog item
- [`catalogItemsDelete`](docs/sdks/catalogitems/README.md#delete) - Delete a catalog item
- [`catalogItemsGet`](docs/sdks/catalogitems/README.md#get) - Get a catalog item
- [`catalogItemsList`](docs/sdks/catalogitems/README.md#list) - List catalog items
- [`catalogItemsUpdate`](docs/sdks/catalogitems/README.md#update) - Update a catalog item
- [`clientsCreate`](docs/sdks/clients/README.md#create) - Create a client
- [`clientsDelete`](docs/sdks/clients/README.md#delete) - Delete a client
- [`clientsGet`](docs/sdks/clients/README.md#get) - Get a client
- [`clientsList`](docs/sdks/clients/README.md#list) - List clients
- [`clientsUpdate`](docs/sdks/clients/README.md#update) - Update a client
- [`contactsCreate`](docs/sdks/contacts/README.md#create) - Create a contact
- [`contactsDelete`](docs/sdks/contacts/README.md#delete) - Delete a contact
- [`contactsGet`](docs/sdks/contacts/README.md#get) - Get a contact
- [`contactsList`](docs/sdks/contacts/README.md#list) - List contacts
- [`contactsUpdate`](docs/sdks/contacts/README.md#update) - Update a contact
- [`contractsCreate`](docs/sdks/contracts/README.md#create) - Create a draft contract
- [`contractsDelete`](docs/sdks/contracts/README.md#delete) - Delete a contract (only drafts)
- [`contractsGet`](docs/sdks/contracts/README.md#get) - Get a contract
- [`contractsList`](docs/sdks/contracts/README.md#list) - List contracts
- [`contractsUpdate`](docs/sdks/contracts/README.md#update) - Update a contract (limited fields)
- [`documentVersionsGet`](docs/sdks/documentversions/README.md#get) - Get a document version
- [`documentVersionsList`](docs/sdks/documentversions/README.md#list) - List document versions
- [`formsAndAgreementsGet`](docs/sdks/formsandagreements/README.md#get) - Get a proposal
- [`formsAndAgreementsList`](docs/sdks/formsandagreements/README.md#list) - List proposals
- [`formsGet`](docs/sdks/forms/README.md#get) - Get a form
- [`formsList`](docs/sdks/forms/README.md#list) - List forms
- [`formSubmissionsGet`](docs/sdks/formsubmissions/README.md#get) - Get a form submission (with answers)
- [`formSubmissionsList`](docs/sdks/formsubmissions/README.md#list) - List form submissions
- [`invoicesCreate`](docs/sdks/invoices/README.md#create) - Create an invoice
- [`invoicesDelete`](docs/sdks/invoices/README.md#delete) - Delete an invoice (only drafts)
- [`invoicesGet`](docs/sdks/invoices/README.md#get) - Get an invoice
- [`invoicesList`](docs/sdks/invoices/README.md#list) - List invoices
- [`invoicesUpdate`](docs/sdks/invoices/README.md#update) - Update an invoice (line items not editable in v1)
- [`milestonesCreate`](docs/sdks/milestones/README.md#create) - Create a milestone
- [`milestonesDelete`](docs/sdks/milestones/README.md#delete) - Delete a milestone
- [`milestonesGet`](docs/sdks/milestones/README.md#get) - Get a milestone
- [`milestonesList`](docs/sdks/milestones/README.md#list) - List milestones
- [`milestonesUpdate`](docs/sdks/milestones/README.md#update) - Update a milestone
- [`paymentsCreate`](docs/sdks/payments/README.md#create) - Record a manual payment
- [`paymentsGet`](docs/sdks/payments/README.md#get) - Get a payment
- [`paymentsList`](docs/sdks/payments/README.md#list) - List payments
- [`paymentsUpdate`](docs/sdks/payments/README.md#update) - Update a payment (notes/reference only — payments are otherwise immutable)
- [`payoutsGet`](docs/sdks/payouts/README.md#get) - Get a payout
- [`payoutsList`](docs/sdks/payouts/README.md#list) - List payouts
- [`projectsCreate`](docs/sdks/projects/README.md#create) - Create a project
- [`projectsDelete`](docs/sdks/projects/README.md#delete) - Delete a project
- [`projectsGet`](docs/sdks/projects/README.md#get) - Get a project
- [`projectsList`](docs/sdks/projects/README.md#list) - List projects
- [`projectsUpdate`](docs/sdks/projects/README.md#update) - Update a project
- [`timeEntriesCreate`](docs/sdks/timeentries/README.md#create) - Create a time entry
- [`timeEntriesDelete`](docs/sdks/timeentries/README.md#delete) - Delete a time entry
- [`timeEntriesGet`](docs/sdks/timeentries/README.md#get) - Get a time entry
- [`timeEntriesList`](docs/sdks/timeentries/README.md#list) - List time entries
- [`timeEntriesUpdate`](docs/sdks/timeentries/README.md#update) - Update a time entry
- [`transactionsCreate`](docs/sdks/transactions/README.md#create) - Create a transaction (expense or charge)
- [`transactionsDelete`](docs/sdks/transactions/README.md#delete) - Delete a transaction
- [`transactionsGet`](docs/sdks/transactions/README.md#get) - Get a transaction
- [`transactionsList`](docs/sdks/transactions/README.md#list) - List transactions
- [`transactionsUpdate`](docs/sdks/transactions/README.md#update) - Update a transaction
- [`webhooksCreate`](docs/sdks/webhooks/README.md#create) - Subscribe to events
- [`webhooksDelete`](docs/sdks/webhooks/README.md#delete) - Delete a webhook
- [`webhooksGet`](docs/sdks/webhooks/README.md#get) - Get a webhook
- [`webhooksList`](docs/sdks/webhooks/README.md#list) - List webhook subscriptions
- [`webhooksUpdate`](docs/sdks/webhooks/README.md#update) - Update a webhook

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Pagination [pagination] -->
## Pagination

Some of the endpoints in this SDK support pagination. To use pagination, you
make your SDK calls as usual, but the returned response object will also be an
async iterable that can be consumed using the [`for await...of`][for-await-of]
syntax.

[for-await-of]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for-await...of

Here's an example of one such pagination call:

```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.clients.list({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Pagination [pagination] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.clients.list(
    {
      apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
    },
    {},
    {
      retries: {
        strategy: "backoff",
        backoff: {
          initialInterval: 1,
          maxInterval: 50,
          exponent: 1.1,
          maxElapsedTime: 100,
        },
        retryConnectionErrors: false,
      },
    },
  );

  for await (const page of result) {
    console.log(page);
  }
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
});

async function run() {
  const result = await clientCasa.clients.list({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`ClientCasaError`](./src/models/errors/client-casa-error.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { ClientCasa } from "@clientcasa/sdk";
import * as errors from "@clientcasa/sdk/models/errors";

const clientCasa = new ClientCasa();

async function run() {
  try {
    const result = await clientCasa.clients.list({
      apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
    }, {});

    for await (const page of result) {
      console.log(page);
    }
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.ClientCasaError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.ApiError) {
        console.log(error.data$.error); // models.ErrorT
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`ClientCasaError`](./src/models/errors/client-casa-error.ts): The base class for HTTP error responses.
  * [`ApiError`](./src/models/errors/api-error.ts): Generic error.

<details><summary>Less common errors (6)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/http-client-errors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/http-client-errors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/http-client-errors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/http-client-errors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/http-client-errors.ts): Unrecognised or unexpected error.


**Inherit from [`ClientCasaError`](./src/models/errors/client-casa-error.ts)**:
* [`ResponseValidationError`](./src/models/errors/response-validation-error.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa({
  serverURL: "https://www.clientcasa.com",
});

async function run() {
  const result = await clientCasa.clients.list({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to:
- route requests through a proxy server using [undici](https://www.npmjs.com/package/undici)'s ProxyAgent
- use the `"beforeRequest"` hook to add a custom header and a timeout to requests
- use the `"requestError"` hook to log errors

```typescript
import { ClientCasa } from "@clientcasa/sdk";
import { ProxyAgent } from "undici";
import { HTTPClient } from "@clientcasa/sdk/lib/http";

const dispatcher = new ProxyAgent("http://proxy.example.com:8080");

const httpClient = new HTTPClient({
  // 'fetcher' takes a function that has the same signature as native 'fetch'.
  fetcher: (input, init) =>
    // 'dispatcher' is specific to undici and not part of the standard Fetch API.
    fetch(input, { ...init, dispatcher } as RequestInit),
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new ClientCasa({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { ClientCasa } from "@clientcasa/sdk";

const sdk = new ClientCasa({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `CLIENTCASA_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

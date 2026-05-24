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
  const result = await clientCasa.clients.listClients({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  console.log(result);
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
  const result = await clientCasa.clients.listClients({}, {});

  console.log(result);
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [CalendarEvents](docs/sdks/calendarevents/README.md)

* [listCalendarEvents](docs/sdks/calendarevents/README.md#listcalendarevents) - List calendar events
* [createCalendarEvent](docs/sdks/calendarevents/README.md#createcalendarevent) - Create a calendar event
* [getCalendarEvent](docs/sdks/calendarevents/README.md#getcalendarevent) - Get a calendar event
* [deleteCalendarEvent](docs/sdks/calendarevents/README.md#deletecalendarevent) - Delete a calendar event
* [updateCalendarEvent](docs/sdks/calendarevents/README.md#updatecalendarevent) - Update a calendar event

### [CatalogItems](docs/sdks/catalogitems/README.md)

* [listCatalogItems](docs/sdks/catalogitems/README.md#listcatalogitems) - List catalog items
* [createCatalogItem](docs/sdks/catalogitems/README.md#createcatalogitem) - Create a catalog item
* [getCatalogItem](docs/sdks/catalogitems/README.md#getcatalogitem) - Get a catalog item
* [deleteCatalogItem](docs/sdks/catalogitems/README.md#deletecatalogitem) - Delete a catalog item
* [updateCatalogItem](docs/sdks/catalogitems/README.md#updatecatalogitem) - Update a catalog item

### [Clients](docs/sdks/clients/README.md)

* [listClients](docs/sdks/clients/README.md#listclients) - List clients
* [createClient](docs/sdks/clients/README.md#createclient) - Create a client
* [getClient](docs/sdks/clients/README.md#getclient) - Get a client
* [deleteClient](docs/sdks/clients/README.md#deleteclient) - Delete a client
* [updateClient](docs/sdks/clients/README.md#updateclient) - Update a client

### [Contacts](docs/sdks/contacts/README.md)

* [listContacts](docs/sdks/contacts/README.md#listcontacts) - List contacts
* [createContact](docs/sdks/contacts/README.md#createcontact) - Create a contact
* [getContact](docs/sdks/contacts/README.md#getcontact) - Get a contact
* [deleteContact](docs/sdks/contacts/README.md#deletecontact) - Delete a contact
* [updateContact](docs/sdks/contacts/README.md#updatecontact) - Update a contact

### [Contracts](docs/sdks/contracts/README.md)

* [listContracts](docs/sdks/contracts/README.md#listcontracts) - List contracts
* [createContract](docs/sdks/contracts/README.md#createcontract) - Create a draft contract
* [getContract](docs/sdks/contracts/README.md#getcontract) - Get a contract
* [deleteContract](docs/sdks/contracts/README.md#deletecontract) - Delete a contract (only drafts)
* [updateContract](docs/sdks/contracts/README.md#updatecontract) - Update a contract (limited fields)

### [Inquiries](docs/sdks/inquiries/README.md)

* [listInquiries](docs/sdks/inquiries/README.md#listinquiries) - List inquiries
* [createInquiry](docs/sdks/inquiries/README.md#createinquiry) - Create an inquiry
* [getInquiry](docs/sdks/inquiries/README.md#getinquiry) - Get an inquiry
* [deleteInquiry](docs/sdks/inquiries/README.md#deleteinquiry) - Delete an inquiry
* [updateInquiry](docs/sdks/inquiries/README.md#updateinquiry) - Update an inquiry

### [Invoices](docs/sdks/invoices/README.md)

* [listInvoices](docs/sdks/invoices/README.md#listinvoices) - List invoices
* [createInvoice](docs/sdks/invoices/README.md#createinvoice) - Create an invoice
* [getInvoice](docs/sdks/invoices/README.md#getinvoice) - Get an invoice
* [deleteInvoice](docs/sdks/invoices/README.md#deleteinvoice) - Delete an invoice (only drafts)
* [updateInvoice](docs/sdks/invoices/README.md#updateinvoice) - Update an invoice (line items not editable in v1)

### [Milestones](docs/sdks/milestones/README.md)

* [listMilestones](docs/sdks/milestones/README.md#listmilestones) - List milestones
* [createMilestone](docs/sdks/milestones/README.md#createmilestone) - Create a milestone
* [getMilestone](docs/sdks/milestones/README.md#getmilestone) - Get a milestone
* [deleteMilestone](docs/sdks/milestones/README.md#deletemilestone) - Delete a milestone
* [updateMilestone](docs/sdks/milestones/README.md#updatemilestone) - Update a milestone

### [Payments](docs/sdks/payments/README.md)

* [listPayments](docs/sdks/payments/README.md#listpayments) - List payments
* [createPayment](docs/sdks/payments/README.md#createpayment) - Record a manual payment
* [getPayment](docs/sdks/payments/README.md#getpayment) - Get a payment
* [updatePayment](docs/sdks/payments/README.md#updatepayment) - Update a payment (notes/reference only — payments are otherwise immutable)

### [Payouts](docs/sdks/payouts/README.md)

* [listPayouts](docs/sdks/payouts/README.md#listpayouts) - List payouts
* [getPayout](docs/sdks/payouts/README.md#getpayout) - Get a payout

### [Projects](docs/sdks/projects/README.md)

* [listProjects](docs/sdks/projects/README.md#listprojects) - List projects
* [createProject](docs/sdks/projects/README.md#createproject) - Create a project
* [getProject](docs/sdks/projects/README.md#getproject) - Get a project
* [deleteProject](docs/sdks/projects/README.md#deleteproject) - Delete a project
* [updateProject](docs/sdks/projects/README.md#updateproject) - Update a project

### [Proposals](docs/sdks/proposals/README.md)

* [listProposals](docs/sdks/proposals/README.md#listproposals) - List proposals
* [createProposal](docs/sdks/proposals/README.md#createproposal) - Create a proposal (metadata only — rich-text content is dashboard-managed)
* [getProposal](docs/sdks/proposals/README.md#getproposal) - Get a proposal
* [deleteProposal](docs/sdks/proposals/README.md#deleteproposal) - Delete a proposal (only drafts)
* [updateProposal](docs/sdks/proposals/README.md#updateproposal) - Update a proposal

### [TimeEntries](docs/sdks/timeentries/README.md)

* [listTimeEntries](docs/sdks/timeentries/README.md#listtimeentries) - List time entries
* [createTimeEntry](docs/sdks/timeentries/README.md#createtimeentry) - Create a time entry
* [getTimeEntry](docs/sdks/timeentries/README.md#gettimeentry) - Get a time entry
* [deleteTimeEntry](docs/sdks/timeentries/README.md#deletetimeentry) - Delete a time entry
* [updateTimeEntry](docs/sdks/timeentries/README.md#updatetimeentry) - Update a time entry

### [Transactions](docs/sdks/transactions/README.md)

* [listTransactions](docs/sdks/transactions/README.md#listtransactions) - List transactions
* [createTransaction](docs/sdks/transactions/README.md#createtransaction) - Create a transaction (expense or charge)
* [getTransaction](docs/sdks/transactions/README.md#gettransaction) - Get a transaction
* [deleteTransaction](docs/sdks/transactions/README.md#deletetransaction) - Delete a transaction
* [updateTransaction](docs/sdks/transactions/README.md#updatetransaction) - Update a transaction

### [Webhooks](docs/sdks/webhooks/README.md)

* [listWebhooks](docs/sdks/webhooks/README.md#listwebhooks) - List webhook subscriptions
* [createWebhook](docs/sdks/webhooks/README.md#createwebhook) - Subscribe to events
* [getWebhook](docs/sdks/webhooks/README.md#getwebhook) - Get a webhook
* [deleteWebhook](docs/sdks/webhooks/README.md#deletewebhook) - Delete a webhook
* [updateWebhook](docs/sdks/webhooks/README.md#updatewebhook) - Update a webhook

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

- [`calendarEventsCreateCalendarEvent`](docs/sdks/calendarevents/README.md#createcalendarevent) - Create a calendar event
- [`calendarEventsDeleteCalendarEvent`](docs/sdks/calendarevents/README.md#deletecalendarevent) - Delete a calendar event
- [`calendarEventsGetCalendarEvent`](docs/sdks/calendarevents/README.md#getcalendarevent) - Get a calendar event
- [`calendarEventsListCalendarEvents`](docs/sdks/calendarevents/README.md#listcalendarevents) - List calendar events
- [`calendarEventsUpdateCalendarEvent`](docs/sdks/calendarevents/README.md#updatecalendarevent) - Update a calendar event
- [`catalogItemsCreateCatalogItem`](docs/sdks/catalogitems/README.md#createcatalogitem) - Create a catalog item
- [`catalogItemsDeleteCatalogItem`](docs/sdks/catalogitems/README.md#deletecatalogitem) - Delete a catalog item
- [`catalogItemsGetCatalogItem`](docs/sdks/catalogitems/README.md#getcatalogitem) - Get a catalog item
- [`catalogItemsListCatalogItems`](docs/sdks/catalogitems/README.md#listcatalogitems) - List catalog items
- [`catalogItemsUpdateCatalogItem`](docs/sdks/catalogitems/README.md#updatecatalogitem) - Update a catalog item
- [`clientsCreateClient`](docs/sdks/clients/README.md#createclient) - Create a client
- [`clientsDeleteClient`](docs/sdks/clients/README.md#deleteclient) - Delete a client
- [`clientsGetClient`](docs/sdks/clients/README.md#getclient) - Get a client
- [`clientsListClients`](docs/sdks/clients/README.md#listclients) - List clients
- [`clientsUpdateClient`](docs/sdks/clients/README.md#updateclient) - Update a client
- [`contactsCreateContact`](docs/sdks/contacts/README.md#createcontact) - Create a contact
- [`contactsDeleteContact`](docs/sdks/contacts/README.md#deletecontact) - Delete a contact
- [`contactsGetContact`](docs/sdks/contacts/README.md#getcontact) - Get a contact
- [`contactsListContacts`](docs/sdks/contacts/README.md#listcontacts) - List contacts
- [`contactsUpdateContact`](docs/sdks/contacts/README.md#updatecontact) - Update a contact
- [`contractsCreateContract`](docs/sdks/contracts/README.md#createcontract) - Create a draft contract
- [`contractsDeleteContract`](docs/sdks/contracts/README.md#deletecontract) - Delete a contract (only drafts)
- [`contractsGetContract`](docs/sdks/contracts/README.md#getcontract) - Get a contract
- [`contractsListContracts`](docs/sdks/contracts/README.md#listcontracts) - List contracts
- [`contractsUpdateContract`](docs/sdks/contracts/README.md#updatecontract) - Update a contract (limited fields)
- [`inquiriesCreateInquiry`](docs/sdks/inquiries/README.md#createinquiry) - Create an inquiry
- [`inquiriesDeleteInquiry`](docs/sdks/inquiries/README.md#deleteinquiry) - Delete an inquiry
- [`inquiriesGetInquiry`](docs/sdks/inquiries/README.md#getinquiry) - Get an inquiry
- [`inquiriesListInquiries`](docs/sdks/inquiries/README.md#listinquiries) - List inquiries
- [`inquiriesUpdateInquiry`](docs/sdks/inquiries/README.md#updateinquiry) - Update an inquiry
- [`invoicesCreateInvoice`](docs/sdks/invoices/README.md#createinvoice) - Create an invoice
- [`invoicesDeleteInvoice`](docs/sdks/invoices/README.md#deleteinvoice) - Delete an invoice (only drafts)
- [`invoicesGetInvoice`](docs/sdks/invoices/README.md#getinvoice) - Get an invoice
- [`invoicesListInvoices`](docs/sdks/invoices/README.md#listinvoices) - List invoices
- [`invoicesUpdateInvoice`](docs/sdks/invoices/README.md#updateinvoice) - Update an invoice (line items not editable in v1)
- [`milestonesCreateMilestone`](docs/sdks/milestones/README.md#createmilestone) - Create a milestone
- [`milestonesDeleteMilestone`](docs/sdks/milestones/README.md#deletemilestone) - Delete a milestone
- [`milestonesGetMilestone`](docs/sdks/milestones/README.md#getmilestone) - Get a milestone
- [`milestonesListMilestones`](docs/sdks/milestones/README.md#listmilestones) - List milestones
- [`milestonesUpdateMilestone`](docs/sdks/milestones/README.md#updatemilestone) - Update a milestone
- [`paymentsCreatePayment`](docs/sdks/payments/README.md#createpayment) - Record a manual payment
- [`paymentsGetPayment`](docs/sdks/payments/README.md#getpayment) - Get a payment
- [`paymentsListPayments`](docs/sdks/payments/README.md#listpayments) - List payments
- [`paymentsUpdatePayment`](docs/sdks/payments/README.md#updatepayment) - Update a payment (notes/reference only — payments are otherwise immutable)
- [`payoutsGetPayout`](docs/sdks/payouts/README.md#getpayout) - Get a payout
- [`payoutsListPayouts`](docs/sdks/payouts/README.md#listpayouts) - List payouts
- [`projectsCreateProject`](docs/sdks/projects/README.md#createproject) - Create a project
- [`projectsDeleteProject`](docs/sdks/projects/README.md#deleteproject) - Delete a project
- [`projectsGetProject`](docs/sdks/projects/README.md#getproject) - Get a project
- [`projectsListProjects`](docs/sdks/projects/README.md#listprojects) - List projects
- [`projectsUpdateProject`](docs/sdks/projects/README.md#updateproject) - Update a project
- [`proposalsCreateProposal`](docs/sdks/proposals/README.md#createproposal) - Create a proposal (metadata only — rich-text content is dashboard-managed)
- [`proposalsDeleteProposal`](docs/sdks/proposals/README.md#deleteproposal) - Delete a proposal (only drafts)
- [`proposalsGetProposal`](docs/sdks/proposals/README.md#getproposal) - Get a proposal
- [`proposalsListProposals`](docs/sdks/proposals/README.md#listproposals) - List proposals
- [`proposalsUpdateProposal`](docs/sdks/proposals/README.md#updateproposal) - Update a proposal
- [`timeEntriesCreateTimeEntry`](docs/sdks/timeentries/README.md#createtimeentry) - Create a time entry
- [`timeEntriesDeleteTimeEntry`](docs/sdks/timeentries/README.md#deletetimeentry) - Delete a time entry
- [`timeEntriesGetTimeEntry`](docs/sdks/timeentries/README.md#gettimeentry) - Get a time entry
- [`timeEntriesListTimeEntries`](docs/sdks/timeentries/README.md#listtimeentries) - List time entries
- [`timeEntriesUpdateTimeEntry`](docs/sdks/timeentries/README.md#updatetimeentry) - Update a time entry
- [`transactionsCreateTransaction`](docs/sdks/transactions/README.md#createtransaction) - Create a transaction (expense or charge)
- [`transactionsDeleteTransaction`](docs/sdks/transactions/README.md#deletetransaction) - Delete a transaction
- [`transactionsGetTransaction`](docs/sdks/transactions/README.md#gettransaction) - Get a transaction
- [`transactionsListTransactions`](docs/sdks/transactions/README.md#listtransactions) - List transactions
- [`transactionsUpdateTransaction`](docs/sdks/transactions/README.md#updatetransaction) - Update a transaction
- [`webhooksCreateWebhook`](docs/sdks/webhooks/README.md#createwebhook) - Subscribe to events
- [`webhooksDeleteWebhook`](docs/sdks/webhooks/README.md#deletewebhook) - Delete a webhook
- [`webhooksGetWebhook`](docs/sdks/webhooks/README.md#getwebhook) - Get a webhook
- [`webhooksListWebhooks`](docs/sdks/webhooks/README.md#listwebhooks) - List webhook subscriptions
- [`webhooksUpdateWebhook`](docs/sdks/webhooks/README.md#updatewebhook) - Update a webhook

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.clients.listClients(
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

  console.log(result);
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
  const result = await clientCasa.clients.listClients({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`ClientCasaError`](./src/models/errors/client-casa-error.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                            |
| ------------------- | ---------- | ------------------------------------------------------ |
| `error.message`     | `string`   | Error message                                          |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                     |
| `error.headers`     | `Headers`  | HTTP response headers                                  |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned. |
| `error.rawResponse` | `Response` | Raw HTTP response                                      |

### Example
```typescript
import { ClientCasa } from "@clientcasa/sdk";
import * as errors from "@clientcasa/sdk/models/errors";

const clientCasa = new ClientCasa();

async function run() {
  try {
    const result = await clientCasa.clients.listClients({
      apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
    }, {});

    console.log(result);
  } catch (error) {
    if (error instanceof errors.ClientCasaError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);
    }
  }
}

run();

```

### Error Classes
**Primary error:**
* [`ClientCasaError`](./src/models/errors/client-casa-error.ts): The base class for HTTP error responses.

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
  const result = await clientCasa.clients.listClients({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  console.log(result);
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

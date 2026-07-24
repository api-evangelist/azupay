# Azupay (azupay)

Azupay is an Australian real-time payments company that moves money over the New Payments Platform (NPP), the account-to-account rails operated by Australian Payments Plus. It is API-first: merchants and platforms embed Azupay to receive payments via PayID (AzupayId), send outbound payments to a PayID or BSB/account number (AzupayOut), and collect recurring or on-demand debits through PayTo mandates and payment agreements (AzupayTo). Azupay also offers Confirmation of Payee (CoP) account checks, batch/file processing, reporting, balance management, and hosted UX apps (Pay by Bank, Disbursements, Subscriptions). Home market is Australia.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/azupay/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/azupay/refs/heads/main/apis.yml)

## Tags

- Payments
- Australia
- Real-Time Payments
- Account-to-Account
- New Payments Platform
- PayID
- PayTo
- Money Transfer
- Confirmation of Payee
- Open Banking

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## API Posture

Azupay ships a genuine, self-serve developer portal at [developer.azupay.com.au](https://developer.azupay.com.au/) (ReadMe-hosted) with guides, a full API reference, a changelog, and a UAT environment. The REST API is served from `https://api.azupay.com.au/v1` (UAT at `https://api-uat.azupay.com.au/v1`). Authentication is by API key in the `Authorization` header — a secret key for charged operations and a distributable key for public-facing calls — with OAuth 2.0 client-credentials (scoped JWT bearer tokens, per-tenant token URL) offered as an additional server-to-server option. Webhooks deliver asynchronous payment status. The reference is published as per-operation OpenAPI 3.0.1 definitions; these were harvested and merged into six product-family specs below.

## APIs

### Azupay PaymentRequest API (AzupayId)

Receive real-time account-to-account payments by creating PayID-addressed payment requests; create, retrieve, search, delete, and refund PaymentRequests.

- **Human URL:** [https://developer.azupay.com.au/docs/receiving-payments](https://developer.azupay.com.au/docs/receiving-payments)
- **Base URL:** `https://api.azupay.com.au/v1`
- [OpenAPI](openapi/azupay-payment-request.yml)
- [API Reference](https://developer.azupay.com.au/reference/createpayidpaymentrequest)

### Azupay Payment API (AzupayOut)

Send outbound NPP payments to a PayID or a BSB and account number, then poll for settlement; search prior payments.

- **Human URL:** [https://developer.azupay.com.au/docs/making-payments](https://developer.azupay.com.au/docs/making-payments)
- **Base URL:** `https://api.azupay.com.au/v1`
- [OpenAPI](openapi/azupay-payment.yml)
- [API Reference](https://developer.azupay.com.au/reference/makepayment)

### Azupay PaymentAgreement & Initiation API (AzupayTo / PayTo)

Establish and manage PayTo payment agreements and initiate eligible debits: create, amend, change status, and search agreements; schedule and initiate payments; refund and search initiations.

- **Human URL:** [https://developer.azupay.com.au/docs/payto-integration-guide](https://developer.azupay.com.au/docs/payto-integration-guide)
- **Base URL:** `https://api.azupay.com.au/v1`
- [OpenAPI](openapi/azupay-payment-agreement.yml)
- [API Reference](https://developer.azupay.com.au/reference/createpaymentagreement)

### Azupay Account Check API (Confirmation of Payee)

Confirm a payee's BSB/account and name via CoP, check NPP/AzupayTo reachability by BSB, and verify PayID registration.

- **Human URL:** [https://developer.azupay.com.au/docs/account-check-cop](https://developer.azupay.com.au/docs/account-check-cop)
- **Base URL:** `https://api.azupay.com.au/v1`
- [OpenAPI](openapi/azupay-check-accounts.yml)
- [API Reference](https://developer.azupay.com.au/reference/checkaccountdetails)

### Azupay Report & Balance API

Retrieve daily transaction reports by month or date range, get time-limited download links, and check current client balance.

- **Human URL:** [https://developer.azupay.com.au/docs/report-api](https://developer.azupay.com.au/docs/report-api)
- **Base URL:** `https://api.azupay.com.au/v1`
- [OpenAPI](openapi/azupay-reports.yml)
- [API Reference](https://developer.azupay.com.au/reference/getreport)

### Azupay Clients & API Key Management API

Manage sub-clients, provision and update sub-merchant API keys, enable/read OAuth 2.0 configuration, and set low-balance alerts.

- **Human URL:** [https://developer.azupay.com.au/docs/clients-api](https://developer.azupay.com.au/docs/clients-api)
- **Base URL:** `https://api.azupay.com.au/v1`
- [OpenAPI](openapi/azupay-configuration.yml)
- [API Reference](https://developer.azupay.com.au/reference/createclient)

## Common Properties

- [Website](https://azupay.com.au/)
- [Developer Portal](https://developer.azupay.com.au/)
- [Documentation](https://developer.azupay.com.au/docs/getting-started-1)
- [Getting Started](https://developer.azupay.com.au/docs/getting-started-1)
- [Sign Up](https://developer.azupay.com.au/docs/signing-up)
- [Changelog](https://developer.azupay.com.au/changelog)
- [Webhooks](https://developer.azupay.com.au/docs/webhooks)
- [Help Center](https://helpcentre.azupay.com.au/)
- [Status Page](https://status.azupay.com.au/)
- [Pricing](https://azupay.com.au/pricing)
- [Blog](https://azupay.com.au/blog)
- [Terms of Service](https://azupay.com.au/terms/)
- [Privacy Policy](https://azupay.com.au/privacy-policy/)
- [Login](https://dashboard.azupay.com.au/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

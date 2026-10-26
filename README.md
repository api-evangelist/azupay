# Azupay (azupay)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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

# Azupay

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

Azupay is an Australian real-time payments company that moves money over the New Payments Platform (NPP), the account-to-account rails operated by Australian Payments Plus. It is API-first: merchants and platforms embed Azupay to receive payments via PayID (AzupayId), send outbound payments to a PayID or BSB/account number (AzupayOut), and collect recurring or on-demand debits through PayTo mandates and payment agreements (AzupayTo). Azupay also offers Confirmation of Payee (CoP) account checks and PayID enquiry to reduce misdirected-payment and fraud risk, batch/file (ABA and SFTP) processing for bulk payouts and collections, reporting, balance management, sub-client and API-key management, and hosted UX apps (Pay by Bank, Disbursements, Subscriptions). Its public developer portal documents a REST API at api.azupay.com.au/v1 with a UAT environment, authenticated by API key (secret and distributable keys in the Authorization header) with OAuth 2.0 client-credentials available as an additional server-to-server option, plus webhooks for asynchronous payment status. Home market is Australia; the surface is genuinely self-serve and documented, though production access and some capabilities (sub-clients, OAuth2) are enabled per client by Azupay.

**Areas:** Payments · Australia · Real-Time Payments · Account-to-Account · New Payments Platform · PayID · PayTo · Money Transfer · Confirmation of Payee · Open Banking

## Azupay on APIs.io

Everything profiled for Azupay is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/azupay/](https://apis.io/providers/azupay/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Azupay API Keys API](https://apis.io/apis/azupay/azupay-api-keys-api/) — Manage API keys for your clients.
- [Azupay Billing and Transaction Reports API](https://apis.io/apis/azupay/azupay-billing-and-transaction-reports-api/) — Fetch transaction, billing and other reports.
- [Azupay Check Accounts API](https://apis.io/apis/azupay/azupay-check-accounts-api/) — Before you submit a Payment you can validate if the PayID or BSB account of the recipient exists and is eligible to receive payments.
- [Azupay Clients API](https://apis.io/apis/azupay/azupay-clients-api/) — Would let you manage clients
- [Azupay Current Balances API](https://apis.io/apis/azupay/azupay-current-balances-api/) — Obtain current dollar balances for Azupay products
- [Azupay Payment Agreement API](https://apis.io/apis/azupay/azupay-payment-agreement-api/) — This API allows you to request Payments using mandates.
- [Azupay Payment Agreement Request API](https://apis.io/apis/azupay/azupay-payment-agreement-request-api/) — This API generates a link to a one-time UX experience that enables payers to create and approve a PayTo Agreement, facilitating the setup of recurring…
- [Azupay Payment API](https://apis.io/apis/azupay/azupay-payment-api/) — This API allows you to make outbound payments to PayID or NPP enabled BSB accounts.
- [Azupay Payment Initiation API](https://apis.io/apis/azupay/azupay-payment-initiation-api/) — This API allows you to initiate Payments using mandates.
- [Azupay Payment Request API](https://apis.io/apis/azupay/azupay-payment-request-api/) — This API allows your customers to make payments using PayID on your website, mobile app or over the counter.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Azupay Webhooks](https://apis.io/asyncapis/azupay/azupay-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [azupay](https://apis.io/servers/azupay/azupay/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Azupay Agentic Access](https://apis.io/agentic-access/azupay/azupay-agentic-access/)

#### JSON Schema (42)

The data models the API reads and writes.

- [AccountCheckObj](https://apis.io/schemas/azupay/azupay-account-check-obj/)
- [AccountCheckResponseObj](https://apis.io/schemas/azupay/azupay-account-check-response-obj/)
- [AccountStatusExtraForPayIdObj](https://apis.io/schemas/azupay/azupay-account-status-extra-for-pay-id-obj/)
- [AccountStatusObj](https://apis.io/schemas/azupay/azupay-account-status-obj/)
- [ApiKeyUpdateObj](https://apis.io/schemas/azupay/azupay-api-key-update-obj/)
- [apiKeysProvisionObj](https://apis.io/schemas/azupay/azupay-api-keys-provision-obj/)
- [apiKeysProvisionResponseObj](https://apis.io/schemas/azupay/azupay-api-keys-provision-response-obj/)
- [BalanceObj](https://apis.io/schemas/azupay/azupay-balance-obj/)
- [BSBEnquiryObj](https://apis.io/schemas/azupay/azupay-bsbenquiry-obj/)
- [ClientObj](https://apis.io/schemas/azupay/azupay-client-obj/)
- [EnableOAuth2ResponseObj](https://apis.io/schemas/azupay/azupay-enable-oauth2-response-obj/)
- [GetApiKeyResponseObj](https://apis.io/schemas/azupay/azupay-get-api-key-response-obj/)
- [GetOAuth2ResponseObj](https://apis.io/schemas/azupay/azupay-get-oauth2-response-obj/)
- [LowBalanceEmailAddresses](https://apis.io/schemas/azupay/azupay-low-balance-email-addresses/)
- [LowBalanceThreshold](https://apis.io/schemas/azupay/azupay-low-balance-threshold/)
- [nextPageIdResponse](https://apis.io/schemas/azupay/azupay-next-page-id-response/)
- [PayIDEnquiryObj](https://apis.io/schemas/azupay/azupay-pay-idenquiry-obj/)
- [PaymentAgreementAmendmentObj](https://apis.io/schemas/azupay/azupay-payment-agreement-amendment-obj/)
- [PaymentAgreementAmendmentStatusObj](https://apis.io/schemas/azupay/azupay-payment-agreement-amendment-status-obj/)
- [PaymentAgreementObj](https://apis.io/schemas/azupay/azupay-payment-agreement-obj/)
- [PaymentAgreementRequestObj](https://apis.io/schemas/azupay/azupay-payment-agreement-request-obj/)
- [PaymentAgreementRequestStatusObj](https://apis.io/schemas/azupay/azupay-payment-agreement-request-status-obj/)
- [PaymentAgreementSearchObj](https://apis.io/schemas/azupay/azupay-payment-agreement-search-obj/)
- [PaymentAgreementStatusObj](https://apis.io/schemas/azupay/azupay-payment-agreement-status-obj/)
- [PaymentInitiationObj](https://apis.io/schemas/azupay/azupay-payment-initiation-obj/)
- …and 17 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Azupay Context](https://apis.io/jsonld/azupay/azupay-context/)

#### Collections (6)

Postman and Open Collection request collections.

- [Azupay Check Accounts API](https://apis.io/collections/azupay/open-azupay-check-accounts/)
- [Azupay Configuration API](https://apis.io/collections/azupay/open-azupay-configuration/)
- [Azupay Payment API](https://apis.io/collections/azupay/open-azupay-payment/)
- [Azupay Payment Agreement API](https://apis.io/collections/azupay/open-azupay-payment-agreement/)
- [Azupay Payment Request API](https://apis.io/collections/azupay/open-azupay-payment-request/)
- [Azupay Reports & Balance API](https://apis.io/collections/azupay/open-azupay-reports/)

#### Overlays (6)

OpenAPI overlays, including conversational phrasing for each operation.

- [Azupay Check Accounts Overlay](https://apis.io/overlays/azupay/azupay-check-accounts-overlay/)
- [Azupay Configuration Overlay](https://apis.io/overlays/azupay/azupay-configuration-overlay/)
- [Azupay Payment Agreement Overlay](https://apis.io/overlays/azupay/azupay-payment-agreement-overlay/)
- [Azupay Payment Overlay](https://apis.io/overlays/azupay/azupay-payment-overlay/)
- [Azupay Payment Request Overlay](https://apis.io/overlays/azupay/azupay-payment-request-overlay/)
- [Azupay Reports Overlay](https://apis.io/overlays/azupay/azupay-reports-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Azupay API Rules](https://apis.io/rules/azupay/azupay-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Azupay Authentication](https://apis.io/security/azupay/azupay-authentication/)
- [Azupay Domain Security](https://apis.io/security/azupay/azupay-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Azupay Scopes](https://apis.io/scopes/azupay/azupay-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Azupay Plans Pricing](https://apis.io/plans/azupay/azupay-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Azupay Rate Limits](https://apis.io/rate-limits/azupay/azupay-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://azupay.com.au/)
- [Documentation](https://developer.azupay.com.au/docs/getting-started-1)
- [Getting started](https://developer.azupay.com.au/docs/getting-started-1)
- [API reference](https://developer.azupay.com.au/reference/createpayidpaymentrequest)
- [Pricing](https://azupay.com.au/pricing)
- [Sign up](https://developer.azupay.com.au/docs/signing-up)
- [Changelog](https://developer.azupay.com.au/changelog)
- [Blog](https://azupay.com.au/blog)
- [Terms of service](https://azupay.com.au/terms/)
- [Privacy policy](https://azupay.com.au/privacy-policy/)
- [Status](https://status.azupay.com.au/)

## API Evangelist rating

**Kin Score 63.3** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 70.2 |
| Contract governance | 22.0 |
| Operational transparency | 42.1 |
| Developer ergonomics | 54.2 |
| Access clarity | 69.7 |

**Agent readiness 59.0** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | — |
| Auth Clarity | served (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 36.2** — Banking & Open Finance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/azupay/](https://apis.io/providers/azupay/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Azupay: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/azupay/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).

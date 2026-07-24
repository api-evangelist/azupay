---
name: Receive a PayID payment
description: Create a PayID-addressed PaymentRequest and confirm the customer has paid.
api: openapi/azupay-payment-request.yml
operations: [createPayIdPaymentRequest, getPaymentRequest, searchPaymentRequest, refundPaymentRequest]
---

# Receive a PayID payment

## Goal
Receive a real-time account-to-account payment from a customer via PayID (AzupayId).

## Auth
Send a Secret (SECR) key in the `Authorization` header, or an OAuth2 bearer token for enabled clients. Base URL `https://api.azupay.com.au/v1` (UAT: `https://api-uat.azupay.com.au/v1`).

## Steps
1. `createPayIdPaymentRequest` (POST /paymentRequest) — supply a unique `clientTransactionId` (your idempotency key), the `paymentAmount`, and optionally a `payID` (else Azupay generates one on a configured domain). Display the returned PayID to the customer to pay from their banking app.
2. Confirm payment. Either subscribe to the `PaymentRequestStatus` webhook (recommended) or poll `getPaymentRequest` (GET /paymentRequest) until `PaymentStatus.status` is `COMPLETE`.
3. Reconcile / search prior requests with `searchPaymentRequest` (POST /paymentRequest/search), paging via `nextPageId`.
4. If a return is required, `refundPaymentRequest` (POST /paymentRequest/refund) with a unique `clientRefundID`.

## Rules
- Re-submitting a create with an already-used `clientTransactionId` returns 409 — treat as a safe duplicate, do not retry blindly.
- Webhooks are at-least-once and can arrive out of order; make your handler idempotent.
- Test in UAT with published PayIDs (e.g. `johnsmith@test.com.au` → SETTLED, `mwilliams@test.com.au` → FAILED).

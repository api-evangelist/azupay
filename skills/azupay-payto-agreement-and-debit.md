---
name: Set up a PayTo agreement and debit it
description: Establish a PayTo mandate and initiate debits against it.
api: openapi/azupay-payment-agreement.yml
operations: [createPaymentAgreementRequest, createPaymentAgreement, changeStatusOfPaymentAgreement, makePaymentInitiation, getPaymentInitiation, refundPaymentInitation, createOrUpdatePaymentScheduler]
---

# Set up a PayTo agreement and debit it

## Goal
Collect recurring or on-demand debits (AzupayTo) via an NPP PayTo mandate.

## Auth
Secret (SECR) key in the `Authorization` header. Base URL `https://api.azupay.com.au/v1`.

## Steps
1. Request a mandate: `createPaymentAgreementRequest` (POST /paymentAgreementRequest) or `createPaymentAgreement` (POST /paymentAgreement). The payer authorises it in their banking app; watch the `PaymentAgreementStatus` webhook for `Active`.
2. (Optional) attach a recurring schedule with `createOrUpdatePaymentScheduler` (POST /paymentAgreement/{paymentAgreementId}/scheduler) — an upsert keyed on `paymentAgreementId`; amendments require the current version (else 412).
3. Debit the agreement: `makePaymentInitiation` (POST /paymentInitiation). Confirm via `getPaymentInitiation` (GET /paymentInitiation) or the `PaymentInitiationStatusEvent` webhook until `SETTLED`.
4. Refund if needed with `refundPaymentInitation` (POST /paymentInitiation/refund).
5. Pause/cancel with `changeStatusOfPaymentAgreement` (POST /paymentAgreement/changeStatus).

## Rules
- Only initiate debits eligible under the mandate terms.
- Scheduler/amendment upserts are version-checked — re-fetch on 412 and retry with the current version.
- Idempotency and out-of-order/at-least-once webhooks apply as elsewhere.

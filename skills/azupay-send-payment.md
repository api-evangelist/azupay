---
name: Send an outbound payment
description: Send an NPP payment to a PayID or BSB/account and confirm settlement.
api: openapi/azupay-payment.yml
operations: [makePayment, getPayment, searchPayment]
---

# Send an outbound payment

## Goal
Send an outbound real-time payment (AzupayOut) to a PayID or a BSB + account number.

## Auth
Requires the Secret (SECR) key — outbound payments are a restricted operation. `Authorization` header. Base URL `https://api.azupay.com.au/v1`.

## Steps
1. `makePayment` (POST /payment) — supply a unique `clientTransactionId`, the `paymentAmount`, and either a `payID` or a `bsb`+`accountNumber` payee. Optionally run Confirmation of Payee first (see the CoP skill).
2. Poll `getPayment` (GET /payment) or subscribe to the `PaymentStatus` webhook until `PaymentStatus.status` is `SETTLED`. Inspect `failureReason` on `FAILED`/`RETURNED`.
3. `searchPayment` (POST /payment/search) to reconcile, paging via `nextPageId`.

## Rules
- Guard the Secret key carefully — it can send money to any Australian bank account.
- `clientTransactionId` is the idempotency key; duplicates return 409.
- UAT: BSB `062000` / account `12345999` → SETTLED, `12345678` → FAILED (AGNT).

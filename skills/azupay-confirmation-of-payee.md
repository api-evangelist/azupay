---
name: Confirm a payee before paying
description: Verify account/PayID details with Confirmation of Payee to reduce misdirected payments.
api: openapi/azupay-check-accounts.yml
operations: [checkAccountDetails, enquireAccount, checkPayID]
---

# Confirm a payee before paying

## Goal
Reduce misdirected-payment and fraud risk by verifying a payee before sending money.

## Auth
`Authorization` header with a Secret or Distributable key. Base URL `https://api.azupay.com.au/v1`.

## Steps
1. For a BSB/account payee: `checkAccountDetails` (POST /accountCheck) — Confirmation of Payee returns a name-match outcome for the supplied BSB, account number and name.
2. To confirm reachability of an account issuer over NPP/AzupayTo: `enquireAccount` (POST /accountEnquiry).
3. For a PayID payee: `checkPayID` (POST /payIDEnquiry) — confirms the PayID is registered and can accept NPP and PayTo payments, and can validate the linked BSB/account.
4. Proceed to `makePayment` only on an acceptable match outcome.

## Rules
- Use CoP as a pre-flight to `makePayment`, not a replacement for your own risk checks.
- Improved joint-account name matching is applied automatically.

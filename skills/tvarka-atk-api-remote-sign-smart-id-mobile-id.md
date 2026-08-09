---
name: Authenticate or sign remotely with Smart-ID or Mobile-ID
description: >-
  Use the server-side remote eID methods - no card, no reader, no device SDK. One create call, a
  verification code to display, then poll or consume the webhook.
api: openapi/tvarka-atk-api-openapi-original.json
generated: '2026-08-09'
method: generated
source: https://atk.tvarka.pro/docs/quickstart/
operations:
  - createAuthRequest
  - createSignRequest
  - getAuthRequest
  - getSignRequest
  - downloadSignedDocument
  - cancelAuthRequest
  - cancelSignRequest
---

# Authenticate or sign remotely with Smart-ID or Mobile-ID

Remote methods complete **server-side**. There is no certificate/complete round trip and no card
driver: you create the request, display the returned `verificationCode`, and wait.

## Authenticate

`createAuthRequest` — `POST /auth/requests` with:

- `method: "smart_id"` plus `personalCode`, or
- `method: "mobile_id"` plus `personalCode` **and** `phoneNumber`
- `audience` is still required and still checked against your approved origins.

Then `getAuthRequest` — `GET /auth/{requestId}` — until `status` is terminal, or consume the signed
webhook.

## Sign

`createSignRequest` — `POST /sign/requests` with `method: "smart_id"` or `"mobile_id"` plus
`personalCode` (and `phoneNumber` for Mobile-ID).

**Remote methods support `format: "pades"` only.** Asking for `asice`, `adoc` or `raw` with a remote
method is not a valid request shape under the `oneOf`, and an unsupported method for your provider
returns **403 `method_not_allowed`**.

Then `getSignRequest` for both axes (`status` and `validation.status`), and
`downloadSignedDocument` with the returned `downloadToken`.

## Rules

- Display `verificationCode` before the person confirms in their Smart-ID or Mobile-ID app — it is
  what stops a signature being slipped onto a different document.
- `personalCode` and `phoneNumber` are **not stored as plaintext request fields** by the provider.
  Do not log them on your side either.
- Remote operations are metered at €0.08 per successful operation versus €0.07 for native ATK.
- Remote test identities are issued with your sandbox credential packet. Do not reuse production
  identities as test fixtures; the `39001010000` / `+37061234567` values in the OpenAPI are schema
  examples, not working fixtures.
- Cancel with `cancelAuthRequest` / `cancelSignRequest` while the request is still non-terminal.

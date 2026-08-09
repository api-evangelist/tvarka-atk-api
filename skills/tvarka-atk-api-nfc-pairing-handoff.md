---
name: Hand a card ceremony off to a phone over NFC
description: >-
  Move an in-flight authentication or signing request from a desktop or server context to the
  holder's phone with a one-claim pairing token, QR payload or deep link.
api: openapi/tvarka-atk-api-openapi-original.json
generated: '2026-08-09'
method: generated
source: https://atk.tvarka.pro/docs/
operations:
  - getAuthPairing
  - getSignPairing
  - claimPairing
  - getAuthRequest
  - getSignRequest
---

# Hand a card ceremony off to a phone over NFC

The pairing surface is what makes the reader optional: the resident taps their eID to an Android
phone instead of plugging in a smart-card reader.

## 1. Get a pairing token (backend, Basic)

- `getAuthPairing` — `GET /auth/{requestId}/pairing`
- `getSignPairing` — `GET /sign/{requestId}/pairing` (rotates and returns a fresh token)

Returns `pairingToken` (high-entropy, **one-claim**, short-lived), `expiresAt`, and three ways to
present it: `pairingUrl`, `qrPayload` and a `deepLink` (`tvarkasign://atk/pair/<token>`).

Render the QR or the deep link. Do not send the `clientToken` itself to the phone — the pairing
token is what crosses the gap.

## 2. Claim it from the phone

`claimPairing` — `POST /pairing/claim`. **This operation is unauthenticated** (`security: []`) —
possession of the token is the credential. Body: `pairingToken` (required), optionally `claimNonce`
and `device`.

Returns `requestId`, `purpose`, a request-scoped `clientToken`, `status` and an optional `summary`
to display before the person taps.

From here the phone continues the normal ceremony: `submitAuthCertificate` / `submitSignCertificate`
then `completeAuth` / `completeSign`, with that `clientToken`.

## 3. Watch it from the backend

Keep polling `getAuthRequest` / `getSignRequest` — the request identity does not change when the
ceremony moves to the phone.

## Failure modes to handle

| Status | Code | Meaning |
|---|---|---|
| 404 | `pairing_not_found` | Unknown or already-purged token |
| 409 | `pairing_not_available` | Pairing not offered for this request/method |
| 409 | `pairing_already_claimed` | One claim only — issue a fresh token |
| 410 | `pairing_expired` | Short-lived; re-fetch and re-render |
| 503 | `pairing_service_unavailable` | Transient; retry |

## Rules

- Treat `pairingToken`, `qrPayload` and `deepLink` as bearer secrets. A QR on a shared screen hands
  the ceremony to whoever photographs it.
- Rotate rather than reuse: `getSignPairing` explicitly rotates the token on each call.
- The token only ever yields a request-scoped `clientToken` — it can never reach your provider Basic
  credential or another request.

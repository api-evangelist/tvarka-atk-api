---
name: Erase request data on demand (GDPR)
description: >-
  Purge one request or every terminal request ahead of the 30-day retention window, and know exactly
  what survives the purge.
api: openapi/tvarka-atk-api-openapi-original.json
generated: '2026-08-09'
method: generated
source: https://atk.tvarka.pro/docs/lifecycle/
operations:
  - deleteAuthRequest
  - deleteSignRequest
  - bulkErasure
---

# Erase request data on demand (GDPR)

Retention defaults to **30 days** per provider and can be reduced by contract. These operations
trigger the same purge earlier. All three take HTTP Basic — they are backend-only.

## Erase one request

- `deleteAuthRequest` — `POST /auth/{requestId}/delete`
- `deleteSignRequest` — `POST /sign/{requestId}/delete`

## Erase in bulk

`bulkErasure` — `POST /erasure` — erases the provider's **terminal** requests. Scoped to your tenant.

## What is removed, and what is not

Removed: document and result bytes, certificates, derived identity data, filenames, messages and
per-request callback details.

**Kept:** a pseudonymous certificate fingerprint and the minimal usage/audit row — retained for
replay prevention, abuse investigation and billing integrity. Say this plainly in your own privacy
notice; an erasure request from a data subject does not delete the billing record.

Separately, remote `personalCode` and `phoneNumber` are never stored as plaintext request fields in
the first place.

## Rules

- **Download before you erase.** `downloadSignedDocument` and `downloadServiceDocument` return
  **404 `document_not_ready`** once the bytes are gone, and the signed container is not recoverable
  from Tvarka afterwards. You are the system of record for the artifact.
- A transient failure of the erasure dependency returns **503 `erasure_failed`** — retry.
- Erasure is irreversible. Treat it as human-authorised, never as an autonomous cleanup step.
- Erasing does not cancel an in-flight ceremony; cancel first with `cancelAuthRequest` /
  `cancelSignRequest`.

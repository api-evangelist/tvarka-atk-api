---
name: Validate, timestamp and archive a signed document
description: >-
  Use the three stateless trust services - check an existing container, add qualified timestamps to
  untimestamped XAdES, or upgrade PAdES B-T to B-LT. All three require an Idempotency-Key.
api: openapi/tvarka-atk-api-openapi-original.json
generated: '2026-08-09'
method: generated
source: https://atk.tvarka.pro/docs/api/
operations:
  - validateDocument
  - timestampDocument
  - archiveDocument
  - downloadServiceDocument
---

# Validate, timestamp and archive a signed document

These three operations are not ceremonies. There is no card, no client token and no polling loop —
you post a document and get a result. **Every one of them requires an `Idempotency-Key` request
header** (1–255 visible characters, scoped to your provider plus that operation).

## Validate

`validateDocument` — `POST /validation`. Body: `format` (required), plus `document` or
`documentRef`, optionally `filename`, `mimeType`, `policy`.

Returns `requestId`, `status` and a `validation` block — `status` (`passed` / `failed` /
`notApplicable`), a `level` such as `QUALIFIED_VALID`, `VALID_NOT_QUALIFIED` or `INDETERMINATE`, and
an optional `report` pointer. Nothing to download.

## Timestamp

`timestampDocument` — `POST /timestamp`. Adds qualified timestamps to untimestamped XAdES
signatures. Returns `requestId`, `status`, `service`, `format`, `timestampedSignatures`, `changed`
and a `downloadToken`.

## Archive

`archiveDocument` — `POST /archive`. Upgrades a PAdES B-T signature to PAdES B-LT for long-term
validation. Returns the same shape plus `archived`, `level` and `signatureField`.

## Download the output

`downloadServiceDocument` — `GET /services/{requestId}/document`, with Basic **or** the one-off
`downloadToken`. Before the output exists you get **404 `document_not_ready`**.

## Idempotency, precisely

- Reuse the **same** `Idempotency-Key` when you retry. That is the documented recovery path for a
  **503** (`Validation/TSA/revocation dependency failed transiently; retry with the same
  Idempotency-Key`).
- The same key with a **different** payload returns **409 `idempotency_conflict`**.
- A call still running under that key returns **409 `service_in_progress`** — wait, do not re-post
  with a new key.
- An idempotent retry does **not** create a second usage event. Rotating the key on every attempt
  turns one €0.07 operation into several.

## Rules

- Billing point is a successfully completed service call, at €0.07 each.
- Document size ceiling is 15 MiB per provider by default (**413 `document_too_large`**).
- A `documentRef` host must be allow-listed (**403 `document_ref_host_not_allowed`**).
- These are the only operations in the API where an agent can safely retry on its own — because the
  idempotency contract makes the retry free and non-duplicating.

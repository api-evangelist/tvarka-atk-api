# Tvarka ATK API (tvarka-atk-api)

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

A single REST API for Lithuanian eID authentication and qualified electronic signing (QES), plus validation, timestamping and long-term-validation (LTV)/archive trust services. The primary ceremonies read the Lithuanian identity card (ATK) through a physical smart-card reader or an NFC phone tap, with Smart-ID and Mobile-ID as optional server-side methods under the same request, polling, webhook and metering model. Signing produces PAdES, ASiC-E, ADOC or detached CAdES artifacts with a qualified timestamp and an advisory validation axis. eIDAS-aligned and EU-resident, operated from Lithuania by Advokato M. Kiskio kontora INVENT and Socialiniai algoritmai, UAB, and priced per successful operation with no subscription or minimum.

**APIs.json:** [https://tvarka-atk-api.apievangelist.com/apis.yml](https://tvarka-atk-api.apievangelist.com/apis.yml)

## Tags

- Authentication
- Digital Signature
- eIDAS
- QES
- Lithuania
- OpenAPI
- eID
- Smart-ID
- Mobile-ID
- NFC
- Timestamping
- LTV
- Webhooks
- Identity
- Trust Services
- GDPR

## Timestamps

- **Created:** 2026-08-02
- **Modified:** 2026-08-09

## APIs

### Tvarka ATK API Auth API

The eID authentication ceremony (`/v1/auth/*`).

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Auth

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-auth-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-auth-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-auth-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API Erasure API

The Erasure API from Tvarka ATK API — 3 operation(s) for erasure.

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Erasure

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-erasure-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-erasure-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-erasure-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API LTV API

Post-signature timestamp and long-term-validation upgrades.

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- LTV

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-ltv-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-ltv-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-ltv-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API Pairing API

NFC remote pairing - complete a request by tapping a card on a different device.

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Pairing

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-pairing-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-pairing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-pairing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API Sign API

The QES signing ceremony (`/v1/sign/*`).

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Sign

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-sign-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-sign-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-sign-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API Tvarka ATK API API

The Tvarka ATK API API from Tvarka ATK API — 0 operation(s) for tvarka atk api.

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Tvarka ATK API

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-tvarka-atk-api-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-tvarka-atk-api-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-tvarka-atk-api-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API Tvarka ATK QES Signing API (paid Tier Addendum) API

The Tvarka ATK QES Signing API (paid Tier Addendum) API from Tvarka ATK API — 0 operation(s) for tvarka atk qes signing api (paid tier addendum).

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Tvarka ATK QES Signing API (paid Tier Addendum)

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-tvarka-atk-qes-signing-api-paid-tier-addendum-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-tvarka-atk-qes-signing-api-paid-tier-addendum-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-tvarka-atk-qes-signing-api-paid-tier-addendum-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API Validation API

Standalone advisory validation of signed artifacts.

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Validation

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-validation-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-validation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-validation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

### Tvarka ATK API Well Known API

Keys for verifying the optional `assertion` JWT.

- **Human URL:** [https://atk.tvarka.pro/docs/](https://atk.tvarka.pro/docs/)
- **Base URL:** `https://atk.tvarka.pro/v1`

#### Tags

- Well-known

#### Properties

- [OpenAPI](openapi/tvarka-atk-api-well-known-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvarka-atk-api-well-known-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvarka-atk-api-well-known-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman Collection](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Documentation](https://atk.tvarka.pro/docs/)
- [A P Is J S O N](https://atk.tvarka.pro/apis.json)

## Common Properties

- [Agentic Access](agentic-access/tvarka-atk-api-agentic-access.yml)
- [Domain Security](security/tvarka-atk-api-domain-security.yml)
- [Authentication](authentication/tvarka-atk-api-authentication.yml)
- [Developer Portal](https://atk.tvarka.pro/docs/)
- [Documentation](https://atk.tvarka.pro/docs/)
- [API Reference](https://atk.tvarka.pro/docs/api/)
- [Getting Started](https://atk.tvarka.pro/docs/quickstart/)
- [Support](https://tvarka.pro/kontaktai/)
- [Sign Up](https://atk.tvarka.pro/docs/access/)
- [Pricing](https://atk.tvarka.pro/docs/pricing/)
- [Terms of Service](https://tvarka.pro/salygos/)
- [Privacy Policy](https://tvarka.pro/privatumas/)
- [Postman](https://atk.tvarka.pro/postman/auth.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Postman](https://atk.tvarka.pro/postman/sign.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Packages](packages/tvarka-atk-api-packages.yml)
- [S D Ks](packages/tvarka-atk-api-packages.yml)
- [Well Known](well-known/tvarka-atk-api-well-known.yml)
- [L L Ms Txt](llms/tvarka-atk-api-llms.txt)
- [M C P Server](mcp/tvarka-atk-api-mcp.yml)
- [Overlay](overlays/tvarka-atk-api-openapi-overlay.yaml)
- [Conformance](conformance/tvarka-atk-api-conformance.yml)
- [Compliance](https://tvarka.pro/saugumas/)
- [Error Catalog](errors/tvarka-atk-api-problem-types.yml)
- [Lifecycle](lifecycle/tvarka-atk-api-lifecycle.yml)
- [Status Page](https://atk.tvarka.pro/status/)
- [Deprecation](https://atk.tvarka.pro/docs/lifecycle/)
- [Changelog](changelog/tvarka-atk-api-changelog.yml)
- [Security](https://tvarka.pro/saugumas/)
- [Vulnerability Disclosure](security/tvarka-atk-api-vulnerability-disclosure.yml)
- [Sandbox](sandbox/tvarka-atk-api-sandbox.yml)
- [Conventions](conventions/tvarka-atk-api-conventions.yml)
- [Idempotency](conventions/tvarka-atk-api-conventions.yml)
- [Webhooks](asyncapi/tvarka-atk-api-webhooks.yml)
- [Data Model](data-model/tvarka-atk-api-data-model.yml)
- [Examples](examples/tvarka-atk-api-examples.yml)
- [Rate Limits](rate-limits/tvarka-atk-api-rate-limits.yml)
- [Plans](plans/tvarka-atk-api-plans.yml)
- [Agent Skill](skills/_index.yml)
- [Arazzo](arazzo/tvarka-atk-api-authenticate-eid-card.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Arazzo](arazzo/tvarka-atk-api-sign-pades-document.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Arazzo](arazzo/tvarka-atk-api-timestamp-and-archive.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)

## Maintainers

**FN:** Tvarka API team
**Email:** info@tvarka.pro
**URL:** https://tvarka.pro

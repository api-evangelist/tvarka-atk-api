# Tvarka ATK API (tvarka-atk-api)

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

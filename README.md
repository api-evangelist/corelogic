# CoreLogic / Cotality (corelogic)

CoreLogic — rebranded as Cotality in 2025 — is a property data and analytics company providing real estate, mortgage, tax, hazard, and climate-risk information across approximately 99% of U.S. residential properties plus operations in Australia, New Zealand, the United Kingdom, Canada, Germany, and India. The company was taken private by Stone Point Capital and Insight Partners in June 2021 in a $6B transaction.

The primary public developer surface is **Trestle** (`trestle-documentation.corelogic.com` / `api.cotality.com`), which delivers MLS listing, member, office, media, and team data via a RESO Web API 2.0 / OData 4.0 endpoint, a RETS 1.8 endpoint, and a Direct Web API for Matrix CRM and MLO integrations. Other Cotality data products — 360 Property Data, Climate Risk Analytics, Discovery Platform — are delivered through cloud data shares (AWS, Databricks, Google Cloud, Azure, Snowflake) and SFTP rather than self-service REST APIs and are gated behind enterprise sales.

**URL:** [Visit APIs.yml URL](https://raw.githubusercontent.com/api-evangelist/corelogic/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party
- **x-type:** company

## Tags

Climate Risk, CoreLogic, Cotality, Direct Web API, Hazard Data, Insurance Data, Listings, Matrix MLS, Mortgage Data, MLS, OData, OneHome, OpenID Connect, Participant Reporting, Property Data, Real Estate, RESO Data Dictionary, RESO Web API, RETS, Tax Data, Trestle

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### Trestle RESO Web API

OData 4.0 / RESO Web API 2.0 endpoint for MLS Property, Member, Office, Media, OpenHouse, Teams, and related resources. OAuth2 Client Credentials against `api.cotality.com/trestle/oidc/connect/token`; 8-hour tokens. RESO Data Dictionary 2.0 with CLIP and UPI identifiers.

- **Base URL:** `https://api.cotality.com/trestle/odata`
- [Documentation](https://trestle-documentation.corelogic.com/webapi.html)
- [API Reference](https://trestle-documentation.corelogic.com/webapi-reference.html)
- [Metadata ($metadata)](https://api.cotality.com/trestle/odata/$metadata)
- [Client Libraries](https://trestle-documentation.corelogic.com/webapi-libraries.html)
- [OpenAPI](openapi/corelogic-trestle-reso-web-api-openapi.yml)
- [Rules](rules/corelogic-trestle-reso-web-api-rules.yml)
- Capabilities: [Property Search](capabilities/trestle-property-search.yaml), [Media Fetch](capabilities/trestle-media-fetch.yaml), [Member & Office Lookup](capabilities/trestle-member-office-lookup.yaml)

### Trestle RETS

RETS 1.8 endpoint over the same Trestle catalog. Session-less; supports HTTP Basic or OAuth2 bearer tokens (scope=rets). Digest auth not supported.

- **Base URL:** `https://api.cotality.com/trestle/rets`
- [Documentation](https://trestle-documentation.corelogic.com/rets.html)

### Direct Web API — CRM

Direct, bidirectional OData connection to the Matrix MLS CRM database. Contacts, EmailHistory, Lists, PortalContents (with AddListingNote / MarkAsViewed / SetListingPreference actions), SavedSearches, UserRegistry, DashboardAPI. Auth: OpenID Connect via Clareity SSO, or HTTP Basic.

- **Base URL:** `https://api.cotality.com/trestle/odata`
- [Documentation](https://trestle-documentation.corelogic.com/direct-webapi-crm-reference.html)
- [OpenAPI](openapi/corelogic-direct-webapi-crm-openapi.yml)
- [Rules](rules/corelogic-direct-webapi-crm-rules.yml)
- Capabilities: [CRM Contacts](capabilities/direct-webapi-crm-contacts.yaml), [Saved Searches](capabilities/direct-webapi-crm-saved-searches.yaml)

### Direct Web API — MLO

Member Loan Officer / lender-side data from Matrix MLS via OData. Integrates originator and loan-officer profiles, branches, and licensing into third-party CRM and lead-routing systems.

- **Base URL:** `https://api.cotality.com/trestle/odata`
- [Documentation](https://trestle-documentation.corelogic.com/direct-webapi-mlo-reference.html)

### Participant Reporting API

For MLS staff and brokerages to report broker/agent participation events back to Trestle. Used for audit, compliance, and royalty/fee-share reporting against listing activity.

- [Documentation (PDF)](https://trestle-documentation.corelogic.com/ParticipantReportingHowTo.pdf)

### 360 Property Data

Enterprise property data product covering structure, ownership, tax, mortgages, hazard risk, climate risk, and geospatial overlays across approximately 99% of U.S. residential properties. Cloud data shares (AWS, Databricks, Google Cloud, Microsoft Azure, Snowflake) and SFTP delivery only.

- [Overview](https://www.cotality.com/360-property-data)

### Climate Risk Analytics

Parcel- and structure-level chronic climate-risk indices and acute peril scores. Chronic Perils covers cold wave, heat wave, extreme precipitation, drought (84 indices, IPCC SSPs to 2030 / 2040 / 2050). Acute Perils covers wildfire, flood, hurricane, severe convective storm, earthquake.

- [Overview](https://www.cotality.com/360-property-data/climate-risk-analytics)

## Common Properties

- [Website](https://www.cotality.com) / [Legacy Website](https://www.corelogic.com)
- [Developer Portal](https://developer.corelogic.com)
- [APAC Developer Portal](https://developer.corelogic.asia/)
- [Documentation](https://trestle-documentation.corelogic.com/)
- [Token Endpoint](https://api.cotality.com/trestle/oidc/connect/token)
- [Client Libraries](https://trestle-documentation.corelogic.com/webapi-libraries.html)
- [FAQ](https://trestle-documentation.corelogic.com/faq.html)
- [Support Email](mailto:trestlesupport@cotality.com)
- [GitHub Organization](https://github.com/corelogic) (no public repos as of 2026-05)
- [Vocabulary](vocabulary/corelogic-vocabulary.yml)
- [JSON-LD Context](json-ld/corelogic-context.jsonld)
- [Plans / Pricing](plans/corelogic-plans-pricing.yml)
- [Rate Limits](rate-limits/corelogic-rate-limits.yml)
- [FinOps](finops/corelogic-finops.yml)

## Artifacts

- **OpenAPI:** 2 specs (`openapi/`)
- **Capabilities:** 5 Naftiko capabilities (`capabilities/`)
- **Rules:** 2 Spectral rulesets (`rules/`)
- **JSON Schema:** 6 schemas (`json-schema/`)
- **JSON Structure:** 1 (`json-structure/`)
- **JSON-LD:** 1 context (`json-ld/`)
- **Examples:** 5 request/response examples (`examples/`)
- **Vocabulary:** 1 (`vocabulary/`)
- **Plans:** 1 (`plans/`)
- **Rate Limits:** 1 (`rate-limits/`)
- **FinOps:** 1 (`finops/`)

## Notable Findings

- The Trestle Web API is migrating its host before end of 2025 — current `api-trestle.corelogic.com` and `api-prod.corelogic.com` will be deprecated in favor of `api.cotality.com`; this profile uses the new host.
- RESO Data Dictionary 2.0 adoption brings CLIP (CoreLogic Linked Identifier for Parcels) and UPI (Universal Parcel Identifier) as cross-MLS keys.
- Direct Web API on Matrix MLS is the operational write-side of the platform — agents' CRM, saved searches, and portal interactions flow through OData CRUD.

## Notable Absences

- No public GitHub repos under the `corelogic` org (0 repos, 260 followers).
- No published self-service pricing; no metered/credit billing.
- No publicly documented per-second rate limits — caps are on result-set size.
- No public OpenAPI specs published by Cotality (the specs in this repo are reverse-engineered from the documentation).
- No documented webhook system for Trestle (replication is poll-based via `ModificationTimestamp`).
- No public status page (third-party `statusgator.com/services/corelogic` monitors 60 components across 6 groups).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

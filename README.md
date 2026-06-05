# CoreLogic (Cotality) (corelogic)

CoreLogic — rebranded as Cotality in 2025 — is a property data and analytics company providing real estate, mortgage, tax, hazard, and climate-risk information across approximately 99% of U.S. residential properties plus operations in Australia, New Zealand, the United Kingdom, Canada, Germany, and India. The company was taken private by Stone Point Capital and Insight Partners in June 2021 in a $6B transaction. The primary public developer surface is Trestle (trestle-documentation.corelogic.com / api.cotality.com), which delivers MLS listing, member, office, media, and team data via a RESO Web API 2.0 / OData 4.0 endpoint, a RETS 1.8 endpoint, and a Direct Web API for Matrix CRM and MLO (member loan officer) integrations. Most other Cotality data products — 360 Property Data, Climate Risk Analytics, Discovery Platform — are delivered through cloud data shares (AWS, Databricks, Google Cloud, Azure, Snowflake) and SFTP rather than self-service REST APIs and are gated behind enterprise sales.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/corelogic/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/corelogic/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Climate Risk
- CoreLogic
- Cotality
- Direct Web API
- Hazard Data
- Insurance Data
- Listings
- Matrix MLS
- Mortgage Data
- MLS
- OData
- OneHome
- OpenID Connect
- Participant Reporting
- Property Data
- Real Estate
- RESO Data Dictionary
- RESO Web API
- RETS
- Tax Data
- Trestle

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### Trestle RESO Web API

Trestle's RESO Web API is an OData 4.0 / RESO Web API 2.0 compliant endpoint that delivers MLS Property, Member, Office, Media, OpenHouse, Teams, TeamMembers, PropertyRooms, PropertyUnitTypes, CustomProperty, Field, Lookup, Model, and HistoryTransactional resources across multiple aggregated U.S. MLSs. Authentication uses OAuth2 Client Credentials against api.cotality.com/trestle/oidc/connect/token with scope=api; tokens are valid for 8 hours. Query support includes $filter, $select, $expand, $orderby, $top (max 1000, or 300000 for key-only), $skip, $count, $apply=groupby (max 10000), Replication=true for 1M+ row datasets, and PrettyEnums=true. Conforms to the RESO Data Dictionary 2.0 and the RESO 2.0 certification including CLIP (machine-learning property identifier) and UPI (Universal Parcel Identifier).

- **Human URL:** [https://trestle-documentation.corelogic.com/webapi.html](https://trestle-documentation.corelogic.com/webapi.html)
- **Base URL:** `https://api.cotality.com/trestle/odata`

#### Tags

- Listings
- MLS
- OData
- Property Data
- RESO Data Dictionary
- RESO Web API
- Trestle

#### Properties

- [Documentation](https://trestle-documentation.corelogic.com/webapi.html)
- [API Reference](https://trestle-documentation.corelogic.com/webapi-reference.html)
- [Getting Started](https://trestle-documentation.corelogic.com/webapi.html)
- [Authorization](https://trestle-documentation.corelogic.com/webapi.html)
- [Client Libraries](https://trestle-documentation.corelogic.com/webapi-libraries.html)
- [Scale](https://trestle-documentation.corelogic.com/webapi-at-scale.html)
- [Metadata](https://api.cotality.com/trestle/odata/$metadata)
- [R E S O Common Format](https://trestle-documentation.corelogic.com/reso-common-format.html)
- [OpenAPI](openapi/corelogic-trestle-reso-web-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/corelogic-trestle-reso-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-trestle-reso-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Rules](rules/corelogic-trestle-reso-web-api-rules.yml)

### Trestle RETS

Trestle's RETS endpoint implements the RETS 1.8 specification on top of the same data catalog as the RESO Web API. The service is session-less; authentication uses HTTP Basic with client credentials or OAuth2 bearer tokens issued from /trestle/oidc/connect/token with scope=rets. Supported transactions include Login, GetMetadata, Search (up to 1000 records per request, default 10), and GetObject for media. The same RESO resources are exposed as RETS SearchType / Class names (Property, Member, Office, Teams, Media, Lookup). Digest authentication is not supported.

- **Human URL:** [https://trestle-documentation.corelogic.com/rets.html](https://trestle-documentation.corelogic.com/rets.html)
- **Base URL:** `https://api.cotality.com/trestle/rets`

#### Tags

- Legacy
- Listings
- MLS
- RETS
- Trestle

#### Properties

- [Documentation](https://trestle-documentation.corelogic.com/rets.html)
- [Client Libraries](https://trestle-documentation.corelogic.com/rets-libraries.html)
- [Connector](https://trestle-documentation.corelogic.com/rets-connector.html)
- [Postman Collection](collections/corelogic-direct-webapi-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-direct-webapi-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/corelogic-trestle-reso-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-trestle-reso-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Direct Web API — CRM

The Direct Web API provides a direct, bidirectional OData connection to the Matrix MLS CRM database. Resources include Contacts, EmailHistory, Lists (carts), PortalContents (with AddListingNote / MarkAsViewed / SetListingPreference actions), SavedSearches, UserRegistry, and a DashboardAPI for aggregated MyListings, HotSheet, MarketWatch, Concierge, and Timeline data. Authentication is OpenID Connect via Clareity Single Sign-On or basic authentication. Standard OData $select / $expand / $orderby / $filter query options are supported.

- **Human URL:** [https://trestle-documentation.corelogic.com/direct-webapi-crm-reference.html](https://trestle-documentation.corelogic.com/direct-webapi-crm-reference.html)
- **Base URL:** `https://api.cotality.com/trestle/odata`

#### Tags

- CRM
- Direct Web API
- Matrix MLS
- OData
- OpenID Connect
- Trestle

#### Properties

- [Documentation](https://trestle-documentation.corelogic.com/direct-webapi-crm-reference.html)
- [OpenAPI](openapi/corelogic-direct-webapi-crm-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/corelogic-direct-webapi-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-direct-webapi-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Rules](rules/corelogic-direct-webapi-crm-rules.yml)

### Direct Web API — MLO

The Direct Web API MLO reference exposes Member Loan Officer / lender-side data from the Matrix MLS platform via OData. Used to integrate originator and loan-officer profiles, branches, and licensing data into third-party CRM and lead-routing systems.

- **Human URL:** [https://trestle-documentation.corelogic.com/direct-webapi-mlo-reference.html](https://trestle-documentation.corelogic.com/direct-webapi-mlo-reference.html)
- **Base URL:** `https://api.cotality.com/trestle/odata`

#### Tags

- Direct Web API
- Lending
- Matrix MLS
- MLO
- OData
- Trestle

#### Properties

- [Documentation](https://trestle-documentation.corelogic.com/direct-webapi-mlo-reference.html)
- [Postman Collection](collections/corelogic-direct-webapi-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-direct-webapi-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/corelogic-trestle-reso-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-trestle-reso-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Participant Reporting API

The Participant Reporting API allows MLS staff and brokerages to report broker/agent participation events back to Trestle. Documented in a published PDF reference; used for audit, compliance, and royalty/fee-share reporting against listing activity.

- **Human URL:** [https://trestle-documentation.corelogic.com/ParticipantReportingHowTo.pdf](https://trestle-documentation.corelogic.com/ParticipantReportingHowTo.pdf)
- **Base URL:** `https://api.cotality.com/trestle/odata`

#### Tags

- Compliance
- MLS
- Participant Reporting
- Reporting
- Trestle

#### Properties

- [Documentation](https://trestle-documentation.corelogic.com/ParticipantReportingHowTo.pdf)
- [Postman Collection](collections/corelogic-direct-webapi-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-direct-webapi-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/corelogic-trestle-reso-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-trestle-reso-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### 360 Property Data

360 Property Data is Cotality's enterprise property data product covering structure, ownership, tax, mortgages, hazard risk, climate risk, and geospatial overlays across approximately 99% of U.S. residential properties. Delivery is via cloud data shares (AWS, Databricks, Google Cloud, Microsoft Azure, Snowflake) and SFTP rather than a self-service REST API; access is gated by enterprise sales contract. Sold to lenders, insurers, government, and proptech platforms.

- **Human URL:** [https://www.cotality.com/360-property-data](https://www.cotality.com/360-property-data)

#### Tags

- Data Share
- Hazard Data
- Mortgage Data
- Property Data
- Tax Data

#### Properties

- [Overview](https://www.cotality.com/360-property-data)
- [Cloud Data Share](https://www.cotality.com/360-property-data)
- [Postman Collection](collections/corelogic-direct-webapi-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-direct-webapi-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/corelogic-trestle-reso-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-trestle-reso-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Climate Risk Analytics

Climate Risk Analytics (CRA) delivers parcel- and structure-level chronic climate risk indices and acute peril scores across the continental United States and the District of Columbia. Chronic Perils covers cold wave, heat wave, extreme precipitation, and drought via 84 indices, with IPCC SSP1-2.6, SSP2-4.5, SSP3-7.0, and SSP5-8.5 scenarios projected to 2030, 2040, and 2050. Acute Perils products cover wildfire, flood, hurricane, severe convective storm, and earthquake. Delivery is via AWS, Databricks, Google Cloud, Azure, Snowflake, and SFTP — semantic companion files ship alongside the data for AI/ML ingestion.

- **Human URL:** [https://www.cotality.com/360-property-data/climate-risk-analytics](https://www.cotality.com/360-property-data/climate-risk-analytics)

#### Tags

- Catastrophe Models
- Climate Risk
- Data Share
- IPCC
- Insurance Data
- Perils

#### Properties

- [Overview](https://www.cotality.com/360-property-data/climate-risk-analytics)
- [Cloud Data Share](https://www.cotality.com/360-property-data/climate-risk-analytics)
- [Postman Collection](collections/corelogic-direct-webapi-crm.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-direct-webapi-crm.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/corelogic-trestle-reso-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/corelogic-trestle-reso-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/corelogic)
- [Website](https://www.cotality.com)
- [Legacy Website](https://www.corelogic.com)
- [Developer Portal](https://developer.corelogic.com)
- [Developer Portal A P A C](https://developer.corelogic.asia/)
- [Documentation](https://trestle-documentation.corelogic.com/)
- [API Reference](https://trestle-documentation.corelogic.com/webapi-reference.html)
- [Getting Started](https://trestle-documentation.corelogic.com/webapi.html)
- [Authorization](https://trestle-documentation.corelogic.com/webapi.html)
- [Token Endpoint](https://api.cotality.com/trestle/oidc/connect/token)
- [Base U R L](https://api.cotality.com/trestle/odata)
- [F A Q](https://trestle-documentation.corelogic.com/faq.html)
- [Client Libraries](https://trestle-documentation.corelogic.com/webapi-libraries.html)
- [Support Email](mailto:trestlesupport@cotality.com)
- [Support Page](https://www.cotality.com/support)
- [Sign In](https://developer.corelogic.asia/user/sign-in)
- [Sign Up](https://developer.corelogic.asia/signup)
- [Vocabulary](vocabulary/corelogic-vocabulary.yml)
- [JSON-LD](json-ld/corelogic-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Plans](plans/corelogic-plans-pricing.yml)
- [Rate Limits](rate-limits/corelogic-rate-limits.yml)
- [Fin Ops](finops/corelogic-finops.yml)
- [Privacy Policy](https://www.cotality.com/privacy-policy)
- [Terms of Service](https://www.cotality.com/terms-of-use)
- [LinkedIn](https://www.linkedin.com/company/cotality)
- [News](https://www.cotality.com/news)
- [L L Ms Txt](https://developer.corelogic.asia/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

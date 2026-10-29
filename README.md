# CoreLogic (Cotality)

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

CoreLogic — rebranded as Cotality in 2025 — is a property data and analytics company providing real estate, mortgage, tax, hazard, and climate-risk information across approximately 99% of U.S. residential properties plus operations in Australia, New Zealand, the United Kingdom, Canada, Germany, and India. The company was taken private by Stone Point Capital and Insight Partners in June 2021 in a $6B transaction. The primary public developer surface is Trestle (trestle-documentation.corelogic.com / api.cotality.com), which delivers MLS listing, member, office, media, and team data via a RESO Web API 2.0 / OData 4.0 endpoint, a RETS 1.8 endpoint, and a Direct Web API for Matrix CRM and MLO (member loan officer) integrations. Most other Cotality data products — 360 Property Data, Climate Risk Analytics, Discovery Platform — are delivered through cloud data shares (AWS, Databricks, Google Cloud, Azure, Snowflake) and SFTP rather than self-service REST APIs and are gated behind enterprise sales.

**Areas:** Climate Risk · CoreLogic · Cotality · Direct Web API · Hazard Data · Insurance Data · Listings · Matrix MLS · Mortgage Data · MLS · OData · OneHome

## CoreLogic (Cotality) on APIs.io

Everything profiled for CoreLogic (Cotality) is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/corelogic/](https://apis.io/providers/corelogic/)** — or go straight to one of the APIs or properties below.

### APIs (27)

- [Trestle RETS](https://apis.io/apis/corelogic/trestle-rets/) — Trestle's RETS endpoint implements the RETS 1.8 specification on top of the same data catalog as the RESO Web API. The service is session-less;…
- [Direct Web API — MLO](https://apis.io/apis/corelogic/direct-webapi-mlo/) — The Direct Web API MLO reference exposes Member Loan Officer / lender-side data from the Matrix MLS platform via OData. Used to integrate originator and…
- [Participant Reporting API](https://apis.io/apis/corelogic/participant-reporting-api/) — The Participant Reporting API allows MLS staff and brokerages to report broker/agent participation events back to Trestle. Documented in a published PDF…
- [360 Property Data](https://apis.io/apis/corelogic/360-property-data/) — 360 Property Data is Cotality's enterprise property data product covering structure, ownership, tax, mortgages, hazard risk, climate risk, and geospatial…
- [Climate Risk Analytics](https://apis.io/apis/corelogic/climate-risk-analytics/) — Climate Risk Analytics (CRA) delivers parcel- and structure-level chronic climate risk indices and acute peril scores across the continental United States…
- [CoreLogic (Cotality) Contacts API](https://apis.io/apis/corelogic/corelogic-contacts-api/) — CRM contact records (name, address, phone, email).
- [CoreLogic (Cotality) DashboardAPI API](https://apis.io/apis/corelogic/corelogic-dashboardapi-api/) — Aggregated dashboard data for the agent home screen.
- [CoreLogic (Cotality) DataSystem API](https://apis.io/apis/corelogic/corelogic-datasystem-api/) — Service-level metadata and available resources.
- [CoreLogic (Cotality) EmailHistory API](https://apis.io/apis/corelogic/corelogic-emailhistory-api/) — Outbound messages sent to contacts.
- [CoreLogic (Cotality) Field API](https://apis.io/apis/corelogic/corelogic-field-api/) — Metadata describing fields available on each resource.
- [CoreLogic (Cotality) HistoryTransactional API](https://apis.io/apis/corelogic/corelogic-historytransactional-api/) — Transactional change history for tracked resources.
- [CoreLogic (Cotality) Lists API](https://apis.io/apis/corelogic/corelogic-lists-api/) — Property lists / carts attached to contacts.
- [CoreLogic (Cotality) Lookup API](https://apis.io/apis/corelogic/corelogic-lookup-api/) — Enumerated lookup values used across resources.
- [CoreLogic (Cotality) Media API](https://apis.io/apis/corelogic/corelogic-media-api/) — Listing media (photos, videos, documents).
- [CoreLogic (Cotality) Member API](https://apis.io/apis/corelogic/corelogic-member-api/) — MLS member (agent) records.
- [CoreLogic (Cotality) Model API](https://apis.io/apis/corelogic/corelogic-model-api/) — Resource model definitions.
- [CoreLogic (Cotality) Office API](https://apis.io/apis/corelogic/corelogic-office-api/) — MLS office (brokerage) records.
- [CoreLogic (Cotality) OpenHouse API](https://apis.io/apis/corelogic/corelogic-openhouse-api/) — Scheduled open-house events.
- [CoreLogic (Cotality) PortalContents API](https://apis.io/apis/corelogic/corelogic-portalcontents-api/) — Contact-scoped listing notes, views, and preferences.
- [CoreLogic (Cotality) Property API](https://apis.io/apis/corelogic/corelogic-property-api/) — MLS property listings and detail records.
- [CoreLogic (Cotality) PropertyRooms API](https://apis.io/apis/corelogic/corelogic-propertyrooms-api/) — Per-room detail for listed properties.
- [CoreLogic (Cotality) PropertyUnitTypes API](https://apis.io/apis/corelogic/corelogic-propertyunittypes-api/) — Per-unit detail for multi-unit properties.
- [CoreLogic (Cotality) Teams API](https://apis.io/apis/corelogic/corelogic-teams-api/) — MLS team records.
- [CoreLogic (Cotality) UserRegistry API](https://apis.io/apis/corelogic/corelogic-userregistry-api/) — Per-user preference key/value store.
- [CoreLogic (Cotality) Custom Property API](https://apis.io/apis/corelogic/corelogic-custom-property-api/) — MLS-specific extensions to the RESO Property resource.
- [CoreLogic (Cotality) Saved Searches API](https://apis.io/apis/corelogic/corelogic-saved-searches-api/) — Saved listing search criteria with auto-email schedules.
- [CoreLogic (Cotality) Team Members API](https://apis.io/apis/corelogic/corelogic-team-members-api/) — Membership relationships between teams and members.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Corelogic Agentic Access](https://apis.io/agentic-access/corelogic/corelogic-agentic-access/)

#### JSON Schema (6)

The data models the API reads and writes.

- [CoreLogic Climate Risk Score](https://apis.io/schemas/corelogic/corelogic-climate-risk/)
- [Direct Web API CRM Contact](https://apis.io/schemas/corelogic/corelogic-contact/)
- [RESO Media](https://apis.io/schemas/corelogic/corelogic-media/)
- [RESO Member](https://apis.io/schemas/corelogic/corelogic-member/)
- [RESO Office](https://apis.io/schemas/corelogic/corelogic-office/)
- [RESO Property](https://apis.io/schemas/corelogic/corelogic-property/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Corelogic Property Structure](https://apis.io/json-structure/corelogic/corelogic-property-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Corelogic Context](https://apis.io/jsonld/corelogic/corelogic-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [CoreLogic / Cotality Vocabulary](https://apis.io/vocabularies/corelogic/corelogic-vocabulary/)

#### Examples (5)

Example requests and responses.

- [Corelogic Climate Risk Score Example](https://apis.io/examples/corelogic/corelogic-climate-risk-score-example/)
- [Corelogic Direct Webapi Create Contact Example](https://apis.io/examples/corelogic/corelogic-direct-webapi-create-contact-example/)
- [Corelogic Trestle Oauth Token Example](https://apis.io/examples/corelogic/corelogic-trestle-oauth-token-example/)
- [Corelogic Trestle Query Media Example](https://apis.io/examples/corelogic/corelogic-trestle-query-media-example/)
- [Corelogic Trestle Query Property Example](https://apis.io/examples/corelogic/corelogic-trestle-query-property-example/)

#### Collections (24)

Postman and Open Collection request collections.

- [CoreLogic Trestle Direct Web API — CRM Contacts API](https://apis.io/collections/corelogic/open-corelogic-contacts-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts CustomProperty API](https://apis.io/collections/corelogic/open-corelogic-customproperty-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts DashboardAPI API](https://apis.io/collections/corelogic/open-corelogic-dashboardapi-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts DataSystem API](https://apis.io/collections/corelogic/open-corelogic-datasystem-api/)
- [CoreLogic Trestle Direct Web API — CRM](https://apis.io/collections/corelogic/open-corelogic-direct-webapi-crm/)
- [CoreLogic Trestle Direct Web API — CRM Contacts EmailHistory API](https://apis.io/collections/corelogic/open-corelogic-emailhistory-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Field API](https://apis.io/collections/corelogic/open-corelogic-field-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts HistoryTransactional API](https://apis.io/collections/corelogic/open-corelogic-historytransactional-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Lists API](https://apis.io/collections/corelogic/open-corelogic-lists-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Lookup API](https://apis.io/collections/corelogic/open-corelogic-lookup-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Media API](https://apis.io/collections/corelogic/open-corelogic-media-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Member API](https://apis.io/collections/corelogic/open-corelogic-member-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Model API](https://apis.io/collections/corelogic/open-corelogic-model-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Office API](https://apis.io/collections/corelogic/open-corelogic-office-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts OpenHouse API](https://apis.io/collections/corelogic/open-corelogic-openhouse-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts PortalContents API](https://apis.io/collections/corelogic/open-corelogic-portalcontents-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Property API](https://apis.io/collections/corelogic/open-corelogic-property-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts PropertyRooms API](https://apis.io/collections/corelogic/open-corelogic-propertyrooms-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts PropertyUnitTypes API](https://apis.io/collections/corelogic/open-corelogic-propertyunittypes-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts SavedSearches API](https://apis.io/collections/corelogic/open-corelogic-savedsearches-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts TeamMembers API](https://apis.io/collections/corelogic/open-corelogic-teammembers-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts Teams API](https://apis.io/collections/corelogic/open-corelogic-teams-api/)
- [CoreLogic Trestle RESO Web API](https://apis.io/collections/corelogic/open-corelogic-trestle-reso-web-api/)
- [CoreLogic Trestle Direct Web API — CRM Contacts UserRegistry API](https://apis.io/collections/corelogic/open-corelogic-userregistry-api/)

#### Governance rules (3)

Spectral rulesets for the provider's contracts.

- [CoreLogic (Cotality) — direct webapi crm rules](https://apis.io/rules/corelogic/corelogic-direct-webapi-crm-rules/)
- [CoreLogic (Cotality) — jsonschema rules](https://apis.io/rules/corelogic/corelogic-jsonschema-spectral-rules/)
- [CoreLogic (Cotality) — trestle reso web api rules](https://apis.io/rules/corelogic/corelogic-trestle-reso-web-api-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Corelogic Authentication](https://apis.io/security/corelogic/corelogic-authentication/)
- [Corelogic Domain Security](https://apis.io/security/corelogic/corelogic-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Corelogic Scopes](https://apis.io/scopes/corelogic/corelogic-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Corelogic Plans Pricing](https://apis.io/plans/corelogic/corelogic-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Corelogic Rate Limits](https://apis.io/rate-limits/corelogic/corelogic-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Corelogic Finops](https://apis.io/finops/corelogic/corelogic-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cotality.com)
- [Documentation](https://trestle-documentation.corelogic.com/)
- [Getting started](https://trestle-documentation.corelogic.com/webapi.html)
- [API reference](https://trestle-documentation.corelogic.com/webapi-reference.html)
- [Blog](https://www.cotality.com/insights)
- [Terms of service](https://www.cotality.com/terms-of-use)
- [Privacy policy](https://www.cotality.com/privacy-policy)
- [GitHub](https://github.com/corelogic)

## API Evangelist rating

**Kin Score 42.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 65.2 |
| Contract quality | 56.1 |
| Contract governance | 27.3 |
| Operational transparency | 10.5 |
| Developer ergonomics | 52.4 |
| Access clarity | 25.0 |

**Agent readiness 23.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 33.3** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/corelogic/](https://apis.io/providers/corelogic/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for CoreLogic (Cotality): the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/corelogic/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).

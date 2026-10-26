# Locus (locus-sh)

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

Locus is an AI-powered last-mile and dispatch logistics platform headquartered in Bengaluru, India (with US operations in Wilmington, Delaware) that helps enterprises plan, execute, and orchestrate deliveries across captive, contracted, outsourced, and hybrid fleets. The platform spans transportation management, dispatch planning and route optimization (across 180+ variables including time, distance, fuel, capacity, and SLAs), hub operations, delivery orchestration and carrier management, fulfillment automation, driver app and control tower track-and-trace, and analytics. Locus claims 360+ enterprise customers across 30+ countries — including Unilever, Nestlé, Blue Dart DHL, Meesho, Lenskart, and Justo — with 1.5B+ deliveries optimized and $320M+ in cost savings generated. The company was acquired by Ingka Group (the world's largest IKEA retailer) in 2024 while continuing to operate as an independent product organization. Locus exposes a SwaggerUI developer surface with three OpenAPI 2.0 specifications covering Order Management (oms.locus-api.com), Entity Management (locus-api.com), and Platform Entities (platform.locus-api.com); authentication is via HTTP Basic plus API key, provisioned by a Locus representative.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/locus-sh/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/locus-sh/refs/heads/main/apis.yml)

## Scope

- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Logistics
- Last Mile Delivery
- Route Optimization
- Dispatch Planning
- Transportation Management
- Fleet Management
- Supply Chain
- Order Management
- Fulfillment
- Track and Trace
- Retail
- E-Commerce
- Artificial Intelligence
- India

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Locus Order Management API

Manage the delivery order lifecycle on the Locus OMS — create, retrieve, cancel, complete, open, park, reschedule, and verify inventory for client orders, plus look up delivery slots and configure service types. Base URL https://oms.locus-api.com/v1.

- **Human URL:** [https://docs.locus.sh/?model=https://docs.locus.sh/apis/locus-oms/v1/order-management.json&host=https://oms.locus-api.com/v1](https://docs.locus.sh/?model=https://docs.locus.sh/apis/locus-oms/v1/order-management.json&host=https://oms.locus-api.com/v1)
- **Base URL:** `https://oms.locus-api.com/v1`

#### Tags

- Order Management
- Orders
- Delivery Slots
- Service Types

#### Properties

- [Documentation](https://docs.locus.sh/?model=https://docs.locus.sh/apis/locus-oms/v1/order-management.json&host=https://oms.locus-api.com/v1)
- [OpenAPI](openapi/locus-oms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/locus-oms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/locus-oms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Sign Up](https://locus.sh/schedule-demo/)

### Locus Entity Management API

Manage core delivery-domain entities on the Locus platform: locations, riders, rider personas, rosters (including auto-create), shift managers, transporters, vehicles, vehicle models, homebases, and line items. Each entity supports create/update, fetch, and disable operations against base URL https://locus-api.com/v1.

- **Human URL:** [https://docs.locus.sh/?model=https://docs.locus.sh/apis/taxy-backend/v1/entities.json&host=https://locus-api.com/v1](https://docs.locus.sh/?model=https://docs.locus.sh/apis/taxy-backend/v1/entities.json&host=https://locus-api.com/v1)
- **Base URL:** `https://locus-api.com/v1`

#### Tags

- Entities
- Riders
- Vehicles
- Locations
- Rosters
- Transporters
- Homebase
- Line Items

#### Properties

- [Documentation](https://docs.locus.sh/?model=https://docs.locus.sh/apis/taxy-backend/v1/entities.json&host=https://locus-api.com/v1)
- [OpenAPI](openapi/locus-entities-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/locus-entities.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/locus-entities.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Sign Up](https://locus.sh/schedule-demo/)

### Locus Platform Entities API

Manage personnel and team master records on the Locus platform service. Provides a compact personnel-create operation, personnel and team status management, and team master upserts against base URL https://platform.locus-api.com/v1.

- **Human URL:** [https://docs.locus.sh/?model=https://docs.locus.sh/apis/platform-service/v1/platform-entities.json&host=https://platform.locus-api.com/v1](https://docs.locus.sh/?model=https://docs.locus.sh/apis/platform-service/v1/platform-entities.json&host=https://platform.locus-api.com/v1)
- **Base URL:** `https://platform.locus-api.com/v1`

#### Tags

- Platform
- Personnel
- Teams

#### Properties

- [Documentation](https://docs.locus.sh/?model=https://docs.locus.sh/apis/platform-service/v1/platform-entities.json&host=https://platform.locus-api.com/v1)
- [OpenAPI](openapi/locus-platform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/locus-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/locus-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Sign Up](https://locus.sh/schedule-demo/)

## Common Properties

- [Website](https://locus.sh)
- [Portal](https://locus.sh)
- [Documentation](https://docs.locus.sh/)
- [API Reference](https://locus.sh/resources/api-references/)
- [Product](https://locus.sh/transportation-management-system/)
- [Product](https://locus.sh/delivery-optimization-software/)
- [Product](https://locus.sh/route-optimization/route-optimization-software/)
- [Product](https://locus.sh/dispatch-management-software/)
- [Product](https://locus.sh/fulfillment-automation/)
- [Product](https://locus.sh/track-and-trace/)
- [Product](https://locus.sh/analytics-and-insights/)
- [Customers](https://locus.sh/customer-success-stories/)
- [Blog](https://locus.sh/blogs/)
- [Newsroom](https://locus.sh/resources/news/)
- [Careers](https://locus.sh/careers/)
- [About Us](https://locus.sh/about-us/)
- [Contact](https://locus.sh/contactus/)
- [Sign Up](https://locus.sh/schedule-demo/)
- [Privacy Policy](https://locus.sh/privacy-policy/)
- [Terms of Service](https://locus.sh/documents/MaraLabsTermsOfUse.pdf)
- [GitHub Organization](https://github.com/locus-sh)
- [LinkedIn](https://www.linkedin.com/company/locus-sh)
- [Twitter](https://twitter.com/Locus_Sh)
- [YouTube](https://www.youtube.com/channel/UCtbHoTbKKmhTAkKu4zY8WKA)
- [Instagram](https://www.instagram.com/locus.sh/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

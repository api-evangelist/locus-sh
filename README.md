# locus-sh

Locus — AI-powered dispatch, route optimization, and last-mile delivery platform (Bengaluru / Wilmington, DE; acquired by Ingka Group in 2024).

## APIs

- **Order Management API** — `https://oms.locus-api.com/v1` — create / cancel / complete / reschedule / park / verify-inventory orders, query delivery slots, configure service types. [openapi/locus-oms-openapi.yml](openapi/locus-oms-openapi.yml)
- **Entity Management API** — `https://locus-api.com/v1` — locations, riders, rider personas, rosters, shift managers, transporters, vehicles, vehicle models, homebases, line items. [openapi/locus-entities-openapi.yml](openapi/locus-entities-openapi.yml)
- **Platform Entities API** — `https://platform.locus-api.com/v1` — personnel and team master records. [openapi/locus-platform-openapi.yml](openapi/locus-platform-openapi.yml)

All three are published as OpenAPI 2.0 (Swagger) specifications. Authentication is HTTP Basic plus an `Authorization` API-key header, provisioned by a Locus representative.

## Links

- Homepage: <https://locus.sh>
- Docs: <https://docs.locus.sh/>
- API references: <https://locus.sh/resources/api-references/>
- GitHub: <https://github.com/locus-sh>

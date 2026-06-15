# Locus (locus-sh)

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

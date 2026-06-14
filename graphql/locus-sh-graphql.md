# Locus GraphQL Schema

## Overview

Locus is an AI-powered last-mile and dispatch logistics platform that helps enterprises plan, execute, and orchestrate deliveries across captive, contracted, outsourced, and hybrid fleets. This conceptual GraphQL schema models the Locus platform's core domain — covering order management, entity management, dispatch planning, route optimization, tracking, proof of delivery, and analytics — as exposed through its REST APIs at oms.locus-api.com, locus-api.com, and platform.locus-api.com.

The schema is derived from the Locus public API documentation at https://docs.locus.sh/ and reflects the three OpenAPI 2.0 specifications (Order Management, Entity Management, and Platform Entities). It is intended as a conceptual reference for understanding the Locus data model and how a GraphQL layer could surface the platform's capabilities.

## Schema Source

- Human URL: https://docs.locus.sh/
- API Reference: https://locus.sh/resources/api-references/
- Order Management API: https://docs.locus.sh/?model=https://docs.locus.sh/apis/locus-oms/v1/order-management.json
- Entity Management API: https://docs.locus.sh/?model=https://docs.locus.sh/apis/taxy-backend/v1/entities.json
- Platform Entities API: https://docs.locus.sh/?model=https://docs.locus.sh/apis/platform-service/v1/platform-entities.json

## Root Types

### Query

- `order(clientId: String!, orderId: String!): Order` — Fetch a single delivery order by client and order ID.
- `orders(clientId: String!, filters: OrderFilters): [Order]` — List orders matching optional filter criteria.
- `deliverySlots(clientId: String!, locationId: String!, serviceType: String): [ServiceType]` — Available delivery time slots for a given location.
- `serviceTypes(clientId: String!): [ServiceType]` — Configured service types for a client.
- `client(clientId: String!): Client` — Fetch client (tenant) details.
- `location(clientId: String!, locationId: String!): Location` — Fetch a delivery location by ID.
- `locations(clientId: String!): [Location]` — List all active locations for a client.
- `driver(clientId: String!, driverId: String!): Driver` — Fetch a rider/driver entity.
- `drivers(clientId: String!, teamId: String): [Driver]` — List drivers, optionally scoped to a team.
- `vehicle(clientId: String!, vehicleId: String!): Vehicle` — Fetch a vehicle entity.
- `vehicles(clientId: String!): [Vehicle]` — List all vehicles for a client.
- `team(clientId: String!, teamId: String!): Team` — Fetch a team/hub entity.
- `teams(clientId: String!): [Team]` — List all teams for a client.
- `trip(clientId: String!, tripId: String!): Trip` — Fetch a trip by ID.
- `trips(clientId: String!, filters: TripFilters): [Trip]` — List trips matching filters.
- `route(clientId: String!, routeId: String!): Route` — Fetch a planned route.
- `tracking(clientId: String!, orderId: String!): Tracking` — Real-time tracking info for an order.
- `zone(clientId: String!, zoneId: String!): Zone` — Fetch a serviceability zone.
- `zones(clientId: String!): [Zone]` — List all zones for a client.
- `serviceability(clientId: String!, geoCoordinate: GeoCoordinateInput!): Serviceability` — Check if a geo-coordinate is serviceable.
- `pod(clientId: String!, orderId: String!): POD` — Fetch proof of delivery for an order.
- `rating(clientId: String!, orderId: String!): Rating` — Fetch customer rating for a delivery.
- `report(clientId: String!, reportType: String!, dateRange: DateRangeInput!): Report` — Fetch an analytics report.
- `webhooks(clientId: String!): [Webhook]` — List configured webhooks for a client.
- `apiKeys(clientId: String!): [APIKey]` — List API keys for a client.

### Mutation

- `createOrder(clientId: String!, input: CreateOrderInput!): Order` — Create a new delivery order.
- `cancelOrder(clientId: String!, orderId: String!): Order` — Cancel an existing order.
- `completeOrder(clientId: String!, orderId: String!): Order` — Mark an order as completed.
- `openOrder(clientId: String!, orderId: String!): Order` — Reopen a parked or cancelled order.
- `parkOrder(clientId: String!, orderId: String!): Order` — Park an order for later dispatching.
- `rescheduleOrder(clientId: String!, orderId: String!, input: RescheduleInput!): Order` — Reschedule an order to a new delivery slot.
- `verifyInventory(clientId: String!, orderId: String!, input: InventoryInput!): Order` — Verify item inventory for an order.
- `createLocation(clientId: String!, input: CreateLocationInput!): Location` — Create or update a delivery location.
- `disableLocation(clientId: String!, locationId: String!): Location` — Disable a location entity.
- `createDriver(clientId: String!, input: CreateDriverInput!): Driver` — Create a new rider/driver entity.
- `updateDriver(clientId: String!, driverId: String!, input: UpdateDriverInput!): Driver` — Update an existing driver.
- `disableDriver(clientId: String!, driverId: String!): Driver` — Disable a driver entity.
- `createVehicle(clientId: String!, input: CreateVehicleInput!): Vehicle` — Create a vehicle entity.
- `updateVehicle(clientId: String!, vehicleId: String!, input: UpdateVehicleInput!): Vehicle` — Update a vehicle.
- `createTeam(clientId: String!, input: CreateTeamInput!): Team` — Create a team/hub.
- `updateTeamStatus(clientId: String!, teamId: String!, status: String!): Team` — Update team active status.
- `createRoster(clientId: String!, input: CreateRosterInput!): ShiftDetails` — Create a roster/shift assignment.
- `autoCreateRoster(clientId: String!, input: AutoRosterInput!): [ShiftDetails]` — Auto-generate roster entries.
- `dispatchTrip(clientId: String!, tripId: String!): Trip` — Dispatch a planned trip to a driver.
- `optimizeRoute(clientId: String!, input: RouteOptimizationInput!): RouteOptimization` — Trigger route optimization.
- `registerWebhook(clientId: String!, input: WebhookInput!): Webhook` — Register a new webhook endpoint.
- `deleteWebhook(clientId: String!, webhookId: String!): Boolean` — Remove a registered webhook.
- `createAPIKey(clientId: String!): APIKey` — Generate a new API key.
- `revokeAPIKey(clientId: String!, keyId: String!): Boolean` — Revoke an API key.

## Domain Areas

### Order Management

The order domain covers the full delivery order lifecycle as managed by the Locus OMS (oms.locus-api.com). Orders are created with item details, delivery address, service type, and time window. They transition through statuses (CREATED, ALLOCATED, IN_TRANSIT, DELIVERED, CANCELLED, PARKED) and carry timestamps for each event. The `OrderDetails` type holds extended fields including item list, line items, special instructions, and proof-of-delivery references.

### Entity Management

Entity management (locus-api.com) covers the master data for the Locus delivery network: Locations (homebases, drop points, pickup points), Drivers/Riders (with personas and roster assignments), Vehicles (with model and capacity), Teams (hubs or branches), Transporters (carrier partners), and Line Items. Entities support create, update, fetch, and disable operations.

### Platform Entities

Platform management (platform.locus-api.com) covers personnel and team master records used across the Locus platform service. This includes compact personnel create operations and team master upserts.

### Dispatch and Route Optimization

Locus's core value proposition is AI-powered dispatch planning and route optimization across 180+ variables. The `RouteOptimization` type models the optimization request and result — including constraints (vehicle capacity, time windows, driver working hours, zone restrictions) and the optimized route output (ordered stop sequence, ETAs per stop, total distance and duration). Trips group an optimized route with an assigned driver and vehicle for actual execution.

### Tracking and POD

The `Tracking` type captures real-time location and status for an in-progress delivery — driver's current geo-coordinate, ETA to next stop, and order status. `POD` (Proof of Delivery) holds the confirmation artifacts: signature image, delivery photo, OTP verification, recipient name, and timestamp.

### Analytics and Reporting

The `Report` and `AnalyticsDetails` types model the reporting surface — aggregated delivery performance metrics, SLA compliance, cost per delivery, on-time delivery rates, and driver performance summaries across configurable date ranges and geographic scopes.

## Types

See `locus-sh-schema.graphql` for the full type definitions.

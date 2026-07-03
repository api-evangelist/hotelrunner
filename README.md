# HotelRunner (hotelrunner)

HotelRunner is a Turkey-founded global hospitality technology platform - a channel manager, central reservation system, booking engine, and website/content manager for hotels, apartments, and travel agencies. Its Custom Apps program exposes a token-authenticated REST API (and a legacy OTA-style XML/SOAP API) so a property's PMS or revenue management system can pull room and rate configuration, push availability/rate/restriction updates to connected OTAs and channels, retrieve and acknowledge reservations, and receive real-time reservation pushes via an HTTP webhook callback.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hotelrunner/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hotelrunner/refs/heads/main/apis.yml)

## Tags

- Hospitality
- Hotel
- Channel Manager
- Booking Engine
- PMS
- Travel

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### HotelRunner Inventory API

Retrieves a property's room types and master rate configuration, and pushes availability, price, stop-sale, min/max stay, and CTA/CTD restriction updates - either for a single room over a date range or in bulk across multiple rooms and up to 90 dates per call - scoped to specific sales channels.

- **Human URL:** [https://developers.hotelrunner.com/custom-apps/rest-api/inventory/get-room-list](https://developers.hotelrunner.com/custom-apps/rest-api/inventory/get-room-list)
- **Base URL:** `https://app.hotelrunner.com/api/v2/apps`

#### Tags

- Rooms
- Rates
- Availability
- Restrictions

#### Properties

- [Documentation](https://developers.hotelrunner.com/custom-apps/rest-api)
- [API Reference](https://developers.hotelrunner.com/custom-apps/rest-api/inventory/get-room-list)
- [OpenAPI](openapi/hotelrunner-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hotelrunner.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hotelrunner.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### HotelRunner Reservations API

Pulls undelivered, modified, or booked reservations (with pagination and date filters), fires confirm/cancel state-change events, and acknowledges delivery of a reservation by its message UID. HotelRunner can also be configured to push new and updated reservations in real time as an outbound HTTP POST webhook to a URL hosted on the connecting PMS.

- **Human URL:** [https://developers.hotelrunner.com/custom-apps/rest-api/reservations/retrieve-reservations](https://developers.hotelrunner.com/custom-apps/rest-api/reservations/retrieve-reservations)
- **Base URL:** `https://app.hotelrunner.com/api/v2/apps`

#### Tags

- Reservations
- Bookings
- Webhooks
- Realtime Push

#### Properties

- [API Reference](https://developers.hotelrunner.com/custom-apps/rest-api/reservations/retrieve-reservations)
- [Documentation](https://developers.hotelrunner.com/custom-apps/rest-api/reservations/realtime-push)
- [OpenAPI](openapi/hotelrunner-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hotelrunner.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hotelrunner.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### HotelRunner Channels API

Lists the OTAs and sales channels connected to a property (Booking.com, Expedia, Airbnb, Online booking engine, and more) along with in-progress, succeeded, and failed update counts for each, so a PMS can monitor channel distribution health.

- **Human URL:** [https://developers.hotelrunner.com/custom-apps/rest-api/channels](https://developers.hotelrunner.com/custom-apps/rest-api/channels)
- **Base URL:** `https://app.hotelrunner.com/api/v2/apps`

#### Tags

- Channels
- Connectivity
- OTA

#### Properties

- [API Reference](https://developers.hotelrunner.com/custom-apps/rest-api/channels)
- [OpenAPI](openapi/hotelrunner-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hotelrunner.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hotelrunner.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### HotelRunner Reference Data API

Read-only lookup endpoints backing property setup and integration mapping - property kinds, room kinds, room amenities, property services and facilities, sellable currencies, ISO country codes, and the master list of connectable OTA channel codes.

- **Human URL:** [https://developers.hotelrunner.com/services/get-currencies](https://developers.hotelrunner.com/services/get-currencies)
- **Base URL:** `https://app.hotelrunner.com`

#### Tags

- Reference Data
- Property Kinds
- Currencies
- Amenities

#### Properties

- [Documentation](https://developers.hotelrunner.com/services/get-currencies)
- [OpenAPI](openapi/hotelrunner-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hotelrunner.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hotelrunner.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/hotelrunner)
- [Website](https://hotelrunner.com/)
- [Documentation](https://developers.hotelrunner.com/)
- [Plans](plans/hotelrunner-plans-pricing.yml)
- [Rate Limits](rate-limits/hotelrunner-rate-limits.yml)
- [Fin Ops](finops/hotelrunner-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

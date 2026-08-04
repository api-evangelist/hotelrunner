# HotelRunner (hotelrunner)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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

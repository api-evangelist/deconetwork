# DecoNetwork (deconetwork)

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

DecoNetwork is web-to-print and business-management software for custom apparel decorators and print shops - screen printing, embroidery, direct-to-garment, and promotional products. It combines branded online stores, quoting, order and artwork management, purchasing, inventory, and production workflow in a single platform, with a global team across the US, UK, and Australia.

For **Enterprise-plan** subscribers, DecoNetwork exposes a documented public JSON API over HTTPS to search and update orders, manage products, manage inventory, and manage purchase orders - so shops can integrate DecoNetwork with external carts, ERP/CRM systems, and custom production automation. The API is request/response REST: requests are sent as query parameters or `application/x-www-form-urlencoded` (a couple of POST bodies are JSON), all responses are JSON carrying a `response_status` object, and each request is authenticated with account `username` and `password` fields.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/deconetwork/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/deconetwork/refs/heads/main/apis.yml)

## Access Model

- The API is **real and publicly documented** at [developer.deconetwork.com](https://www.deconetwork.com/developer-resources/), but **plan-gated**: API access is included **only on the Enterprise plan** (published at USD 399/month plus a one-time license fee). Standard and Premium plans do not include API access.
- Because each merchant runs on their own DecoNetwork site, the developer reference documents the host as `www.deconetwork.com`; callers substitute their own site domain.
- The endpoints captured here are transcribed directly from DecoNetwork's published developer reference - none are fabricated. DecoNetwork also references an Inventory Events Management API whose exact endpoint paths were not resolvable at capture time, so it was deliberately omitted rather than modeled.

## Tags

- Custom Apparel
- Web to Print
- Print Shop Management
- Orders
- Products
- Inventory
- Production Workflow
- E-commerce

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### DecoNetwork Order Management API

Search, analyze, and update orders in a DecoNetwork site. Find orders with multi-condition filtering, sorting, and pagination (up to 100 results per request), optionally including workflow, purchase order, shipment, and production file data, and batch-update order or line-item status to Produced or Shipped.

- **API Reference:** [Order Management API](https://developer.deconetwork.com/documents/api/json/order_management/api.html)
- **Base URL:** `https://www.deconetwork.com/api/json/manage_orders`
- `GET /api/json/manage_orders/find`
- `POST /api/json/manage_orders/update_order_status`

### DecoNetwork Product Management API

Build apps and integrations for managing DecoNetwork products. Search products with multiple conditions joined by logical AND (up to 100 results per request, offset pagination, ISO-8601 UTC date filtering) and retrieve one or more products by ID.

- **API Reference:** [Product Management API](https://developer.deconetwork.com/documents/api/json/product_management/api.html)
- **Base URL:** `https://www.deconetwork.com/api/json/manage_products`
- `POST /api/json/manage_products/find`
- `GET /api/json/manage_products/get`

### DecoNetwork Inventory Management API

Manage DecoNetwork inventory across catalog and custom products. Search SKU-based inventory with search conditions and pagination, and update inventory levels and related settings for SKUs.

- **API Reference:** [Inventory Management API](https://developer.deconetwork.com/documents/api/json/inventory_management/api.html)
- **Base URL:** `https://www.deconetwork.com/api/json/manage_inventory`
- `GET /api/json/manage_inventory/find`
- `POST /api/json/manage_inventory/update`

### DecoNetwork Purchase Order Management API

Retrieve purchase orders by search parameters (up to 100 rows per request) and record stock receipt against purchase orders and customer orders.

- **API Reference:** [Purchase Order Management API](https://developer.deconetwork.com/documents/api/json/purchase_order_management/api.html)
- **Base URL:** `https://www.deconetwork.com/api/json/manage_purchase_orders`
- `GET /api/json/manage_purchase_orders/find`
- `POST /api/json/manage_purchase_orders/receive_stock`

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/deconetwork)
- [Website](https://www.deconetwork.com)
- [Documentation](https://www.deconetwork.com/developer-resources/)
- [Sign Up / Pricing](https://www.deconetwork.com/pricing/)
- [Plans](plans/deconetwork-plans-pricing.yml)
- [Rate Limits](rate-limits/deconetwork-rate-limits.yml)
- [Fin Ops](finops/deconetwork-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

# DecoNetwork (deconetwork)

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

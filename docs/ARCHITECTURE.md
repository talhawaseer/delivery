# Architecture

```text
Android (Kotlin / Compose) ----                                -> Django REST API -> PostgreSQL
Web (React / TypeScript) -------/
```

The web app contains customer storefront routes and staff/admin routes.
Both clients use the same versioned REST API. Django owns authentication,
authorization, pricing, inventory, order state transitions and persistence.

## Suggested API groups
- `/api/v1/auth/`
- `/api/v1/categories/`
- `/api/v1/products/`
- `/api/v1/cart/`
- `/api/v1/orders/`
- `/api/v1/staff/`

Publish an OpenAPI schema from DRF (for example with `drf-spectacular`) and
use it as the contract for both clients.

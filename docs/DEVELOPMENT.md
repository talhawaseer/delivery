# Development guide

## Recommended implementation order
1. Confirm requirements, user roles and order lifecycle.
2. Design database entities and API contracts.
3. Implement Django models, permissions, validation and API.
4. Implement the React storefront/admin against the API.
5. Implement the Android customer app against the same API.
6. Test end-to-end workflows and deploy.

## Core roles
- Customer
- Administrator / staff
- Optional delivery operator (can be represented as a staff permission in v1)

## Core workflows
- Browse/search products and categories
- Manage cart
- Place cash-on-delivery order
- View own order and status
- Staff manage products, inventory, orders and delivery status

## Non-negotiable backend rules
- Recalculate prices on the server; never accept client totals as authoritative.
- Check stock and create orders within database transactions.
- Enforce object-level permissions: customers can only read their own orders.
- Keep an order-item snapshot of product name and unit price at purchase time.
- Validate every status transition on the server.
- Store credentials and signing keys outside source control.

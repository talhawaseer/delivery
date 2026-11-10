# API contract

Keep endpoint names, request/response schemas and error formats documented here
or in the generated OpenAPI document.

Initial resources:
- Auth and customer profile
- Categories and products
- Cart
- Orders and order items
- Staff inventory and order operations

Use consistent pagination and validation error responses. Do not expose Django
model internals directly as an accidental public API contract.

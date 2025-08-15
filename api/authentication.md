# Authentication

- Method: JWT (JSON Web Token)
- Users must authenticate with a login endpoint (not covered here, assumed)
- Each request to protected endpoints requires `Authorization: Bearer <token>` header
- JWT contains user ID, expiration, and roles
- Token expiration: 1 hour
- Errors:
  - 401 Unauthorized if token is missing, expired or invalid
  - 403 Forbidden if user lacks permission

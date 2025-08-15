 # Error Handling and Status Codes

- 200 OK — Successful GET, PUT requests
- 201 Created — Successful POST requests
- 204 No Content — Successful DELETE requests
- 400 Bad Request — Client sent invalid data or malformed request
- 401 Unauthorized — Authentication failed or missing token
- 403 Forbidden — Authenticated but no permission
- 404 Not Found — Resource with given ID does not exist
- 500 Internal Server Error — Unexpected server error

All error responses include JSON with:

```json
{
  "error": "Error message description"
}

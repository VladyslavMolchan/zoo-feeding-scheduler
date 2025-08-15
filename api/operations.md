 # API Operations

## Animals

- **GET /animals**

  - Description: Get list of animals
  - Query Params:
    - `page` (integer, optional) — page number for pagination
    - `size` (integer, optional) — number of items per page
    - `species` (string, optional) — filter by species
  - Response: 200 OK
  - Pagination headers included (`X-Total-Count`)

- **GET /animals/{id}**

  - Description: Get animal by ID
  - Response:
    - 200 OK if found
    - 404 Not Found if not

- **POST /animals**

  - Description: Create a new animal
  - Body: JSON with `name`, `species`, `age`
  - Response:
    - 201 Created on success
    - 400 Bad Request for invalid data

- **PUT /animals/{id}**

  - Description: Update animal info
  - Body: JSON with any of `name`, `species`, `age`
  - Response:
    - 200 OK on success
    - 400 Bad Request for invalid data
    - 404 Not Found if animal doesn't exist

- **DELETE /animals/{id}**

  - Description: Delete an animal
  - Response:
    - 204 No Content on success
    - 404 Not Found if not found

## FeedingSchedules

- Similar CRUD endpoints with pagination and filtering by `animalId` and `feedingTime`

## NutritionAlerts

- GET /alerts with filtering by `animalId` and date range

---

## Status Codes

- 200 OK — successful retrieval or update
- 201 Created — successful creation
- 204 No Content — successful deletion
- 400 Bad Request — validation or client error
- 401 Unauthorized — missing/invalid auth token
- 404 Not Found — resource not found
- 500 Internal Server Error — unexpected error

# Crew - Rate Details

## Get Crew Rate Details

### HTTP Request

```http
GET /api/crew/crew-rate/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
    "id": 5,
    "standardRate": null,
    "negotiation": true,
    "crew": 22
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found

    ```json
    {
    "detail": "No CrewRate matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Crew Rate

### HTTP Request

```http
PUT /api/crew/crew-rate/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "standardRate": 1000,
    "negotiation": false
}
```

### Response Body

```json
{
    "id": 5,
    "standardRate": 1000,
    "negotiation": false,
    "crew": 22
}
```

### Response Status

- **200** - OK
- **400** - Bad Request
  - Invalid data
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

### Issues

- crew field is not updatable but it is present in the request body. It should be removed from the request body.

## Delete Crew Rate

### HTTP Request

```http
DELETE /api/crew/crew-rate/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Status

- **200** - OK
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

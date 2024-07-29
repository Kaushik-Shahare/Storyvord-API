# Crew - Endorsement Details

## Get Crew Endorsement Details

### HTTP Request

```http
GET /api/crew/endorsement-from-peers/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
    "id": 3,
    "text": "Text",
    "givenBy": "givenBy",
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
    "detail": "No Endorsement matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Crew Endorsement

### HTTP Request

```http
PUT /api/crew/endorsement-from-peers/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "text": "Text",
    "givenBy": "givenBy",
    "crew": 22
}
```

### Response Body

```json
{
    "id": 3,
    "text": "Text",
    "givenBy": "givenBy",
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
    "detail": "No Endorsement matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **503** - Gateway Timeout

## Delete Crew Endorsement

### HTTP Request

```http
DELETE /api/crew/endorsement-from-peers/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Status

- **204** - No Content
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found

    ```json
    {
    "detail": "Not found."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

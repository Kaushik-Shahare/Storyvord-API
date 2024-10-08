# Crew - Credit Details

## Get Credit Details

### HTTP Request

```http
GET /api/crew/crew-credits/{creditId}
```

### Request Headers

- **Authorization**: Bearer {token}

### Response Body

```json
{
    "id": 8,
    "title": "Crew Title",
    "year": "2 years",
    "role": "xyz",
    "production": "abc",
    "client": null,
    "type_of_content": "Film",
    "tags": null,
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
    "detail": "No CrewCredits matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Credit Details

### HTTP Request

```http
PUT /api/crew/crew-credits/{creditId}
```

### Request Headers

- **Authorization**: Bearer {token}

### Request Body

```json
{
    "title": "Crew Title",
    "year": "2 years",
    "role": "xyz",
    "production": "abc",
    "client": null,
    "type_of_content": "Film",
    "tags": null,
    "crew": 22
}
```

### Response Body

```json
{
    "id": 8,
    "title": "Crew Title",
    "year": "2 years",
    "role": "xyz",
    "production": "abc",
    "client": null,
    "type_of_content": "Film",
    "tags": null,
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
    "detail": "No CrewCredits matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Delete Credit Details

### HTTP Request

```http
DELETE /api/crew/crew-credits/{creditId}
```

### Request Headers

- **Authorization**: Bearer {token}

### Response Status

- **204** - No Content
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

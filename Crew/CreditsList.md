# Crew - Credits List

## Get Crew Credits List

### HTTP Request

```http
GET /api/crew/crew-credits/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
  {
    "crew": 1,
    "title": "Crew Title",
    "year": "2 years",
    "role": "xyz",
    "production": "abc",
    "client": null,
    "type_of_content": "Film",
    "tags": null
  }
]
```

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

## Create Crew Credit

### HTTP Request

```http
POST /api/crew/crew-credits/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
  "crew": 1,
  "title": "Crew Title",
  "year": "2 years",
  "role": "xyz",
  "production": "abc",
  "client": null,
  "type_of_content": "Film",
  "tags": null
}
```

### Response Body

```json
{
  "id": 3,
  "title": "Crew Title",
  "year": "2 years",
  "role": "xyz",
  "production": "abc",
  "client": null,
  "type_of_content": "Film",
  "tags": null,
  "crew": 1
}
```

### Response Status

- **201** - Created
- **400** - Bad Request
  - Required fields are missing
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

# Crew - Social Links List

## Get Crew Social Links List

### HTTP Request

```http
GET /api/crew/social-links/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 1,
        "link": "https://www.facebook.com",
        "crew": 22
    },
    {
        "id": 2,
        "link": "https://www.instagram.com",
        "crew": 22
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

    ```json
    {
    "detail": "No Social Link matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Create Crew Social Link

### HTTP Request

```http
POST /api/crew/social-links/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "link": "https://www.facebook.com",
    "crew": 22
}
```

### Response Body

```json
{
    "id": 3,
    "link": "https://www.facebook.com",
    "crew": 22
}
```

### Response Status

- **201** - Created
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

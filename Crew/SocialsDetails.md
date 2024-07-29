# Crew - Social Links Details

## Get Crew Social Link Details

### HTTP Request

```http
GET /api/crew/social-links/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
    "id": 1,
    "link": "https://www.facebook.com",
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
     "detail": "No SocialLinks matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Crew Social Link

### HTTP Request

```http
PUT /api/crew/social-links/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "link": "https://www.facebook.com"
}
```

### Response Body

```json
{
    "id": 1,
    "link": "https://www.facebook.com",
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
     "detail": "No SocialLinks matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

### Issues

- Can we edit the crew id?

## Delete Crew Social Link

### HTTP Request

```http
DELETE /api/crew/social-links/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Status

- **204** - No Content
  - Successfully deleted
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found

    ```json
    {
     "detail": "No SocialLinks matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

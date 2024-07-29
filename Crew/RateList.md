# Crew - Rate List

## Get Crew Rate List

### HTTP Request

```http
GET /api/crew/crew-rate/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 5,
        "standardRate": null,
        "negotiation": true,
        "crew": 22
    },
    {
        "id": 6,
        "standardRate": null,
        "negotiation": true,
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
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Create Crew Rate

### HTTP Request

```http
POST /api/crew/crew-rate/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "standardRate": 1000,
    "negotiation": true,
    "crew": 22
}
```

### Response Body

```json
{
    "id": 7,
    "standardRate": 1000,
    "negotiation": true,
    "crew": 22
}
```

### Response Status

- **201** - Created
- **400** - Bad Request
  - Invalid data
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

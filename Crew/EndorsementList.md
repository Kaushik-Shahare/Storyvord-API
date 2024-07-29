# Crew - Endorsement List

## Get Crew Endorsement List

### HTTP Request

```http
GET /api/crew/endorsement-from-peers/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 3,
        "text": "Text",
        "givenBy": "givenBy",
        "crew": 22
    },
    {
        "id": 4,
        "text": "Text",
        "givenBy": "givenBy",
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
    "detail": "No Endorsement matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Create Crew Endorsement

### HTTP Request

```http
POST /api/crew/endorsement-from-peers/
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
    "id": 5,
    "text": "Text",
    "givenBy": "givenBy",
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

# Crew - File Management Details

## Get File Details

### HTTP Request

```http
GET /api/files/{file_id}
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
    "id": 8,
    "file": null,
    "project": "3362a725-ca3c-4499-9f58-a798b34d9926",
    "allowed_users": [
        1,
        2,
        34,
        22
    ]
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update File Details

### HTTP Request

```http
PUT /api/files/{file_id}
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "file": "file",
    "add_users": [1, 2, 6, 3],
    "remove_users": [3, 6],
    "project": null
}
```

### Response Body

```json
{
    "id": 8,
    "file": "file",
    "project": "3362a725-ca3c-4499-9f58-a798b34d9926",
    "allowed_users": [
        1,
        2,
        34,
        22
    ]
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Delete File

### HTTP Request

```http
DELETE /api/files/{file_id}
```

### Request Headers

- **Authorization** - Bearer token

### Response Status

- **204** - No Content
- **401** - Unauthorized
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

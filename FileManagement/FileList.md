# File Management - Files List

## Get Files List

### HTTP Request

```http
GET /api/files
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
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
    },
    {
        "id": 9,
        "file": null,
        "project": "3362a725-ca3c-4499-9f58-a798b34d9926",
        "allowed_users": [
            1,
            2,
            34,
            22
        ]
    }
]
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Upload File

### HTTP Request

```http
POST /api/files
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
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

- **Note**: File should be in base64 format.

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

- **201** - Created
- **401** - Unauthorized
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

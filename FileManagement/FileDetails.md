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
    "id": 26,
    "name": "Cv",
    "file": null,
    "folder": 2
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
    "name": "Name",
}
```

### Response Body

```json
{
    "id": 26,
    "name": "Cv",
    "file": null,
    "folder": 2
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

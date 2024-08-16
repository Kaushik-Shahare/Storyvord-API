# File Management - File List

## Get all files in a folder

### HTTP Request

```http
GET /api/files/folders/files/{folder_id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 31,
        "name": "Cvvv",
        "file": null,
        "folder": 2
    },
    {
        "id": 32,
        "name": "Cvvvd",
        "file": null,
        "folder": 2
    }
]
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **404** - Not Found
- **403** - Forbidden
- **400** - Bad Request
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Upload File in a folder

### HTTP Request

```http
POST /api/files/folders/files/{folder_id}/
```

### Request Headers

- **Authorization** - Bearer token
- **Content-Type** - multipart/form-data

### Request Body

- **project** - String
- **name** - String
- **allowed_users** - List
- **file** - File

### Response Body

```json
{
    "id": 29,
    "name": "Cvv",
    "file": null // Base64 encoded file
}
```

### Response Status

- **201** - Created
- **401** - Unauthorized
- **404** - Not Found
- **403** - Forbidden
- **400** - Bad Request
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

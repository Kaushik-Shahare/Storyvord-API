# File Management - File List

## Get all files in a folder

### HTTP Request

```http
GET /api/files/crew/folders/files/{folder_id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 2,
        "description": null,
        "icon": "2024-07-30 19:11:54.467495+00:00",
        "name": "Folder 1",
        "project": "3362a725-ca3c-4499-9f58-a798b34d9926",
        "default": false,
        "files": [
            {
                "id": 26,
                "allowed_users": [
                    1,
                    2,
                    34
                ],
                "name": "Cv",
                "file": null,
                "folder": 2
            }
        ]
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
POST /api/files/crew/folders/files/{folder_id}/
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
    "allowed_users": [
        34
    ],
    "name": "Cvv",
    "file": null,
    "folder": 3
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

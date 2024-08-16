# File Management - Folder

## Get all folders of a project

### HTTP Request

```http
GET /api/files/folders/{project_id}
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 72,
        "description": "You can find everything related to development here.",
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-square-plus\"><rect width=\"18\" height=\"18\" x=\"3\" y=\"3\" rx=\"2\"></rect><path d=\"M8 12h8\"></path><path d=\"M12 8v8\"></path></svg>",
        "name": "Scripts & Development",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": true,
        "allowed_users": [],
        "created_by": 5
    },
    {
        "id": 74,
        "description": null,
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-book-open-text\"><path d=\"M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z\"></path><path d=\"M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z\"></path><path d=\"M6 8h2\"></path><path d=\"M6 12h2\"></path><path d=\"M16 8h2\"></path><path d=\"M16 12h2\"></path></svg>",
        "name": "Folder 6",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": false,
        "allowed_users": [
            5,
            34
        ],
        "created_by": 5
    },
    {
        "id": 87,
        "description": null,
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-book-open-text\"><path d=\"M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z\"></path><path d=\"M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z\"></path><path d=\"M6 8h2\"></path><path d=\"M6 12h2\"></path><path d=\"M16 8h2\"></path><path d=\"M16 12h2\"></path></svg>",
        "name": "Folder 78",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": false,
        "allowed_users": [
            5
        ],
        "created_by": 5
    },
    {
        "id": 71,
        "description": "You can find contracts for actors, insurances, and more here.",
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-book-open-text\"><path d=\"M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z\"></path><path d=\"M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z\"></path><path d=\"M6 8h2\"></path><path d=\"M6 12h2\"></path><path d=\"M16 8h2\"></path><path d=\"M16 12h2\"></path></svg>",
        "name": "Contracts",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": true,
        "allowed_users": [],
        "created_by": 5
    },
    {
        "id": 75,
        "description": null,
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-book-open-text\"><path d=\"M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z\"></path><path d=\"M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z\"></path><path d=\"M6 8h2\"></path><path d=\"M6 12h2\"></path><path d=\"M16 8h2\"></path><path d=\"M16 12h2\"></path></svg>",
        "name": "Folder 6",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": false,
        "allowed_users": [
            5,
            34
        ],
        "created_by": 5
    },
    {
        "id": 73,
        "description": "You can find copies of your call sheets here after sending them to your crew.",
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-file-spreadsheet\"><path d=\"M15 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7Z\"></path><path d=\"M14 2v4a2 2 0 0 0 2 2h4\"></path><path d=\"M8 13h2\"></path><path d=\"M14 13h2\"></path><path d=\"M8 17h2\"></path><path d=\"M14 17h2\"></path></svg>",
        "name": "Sent Call Sheets",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": true,
        "allowed_users": [],
        "created_by": 5
    },
    {
        "id": 76,
        "description": null,
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-book-open-text\"><path d=\"M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z\"></path><path d=\"M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z\"></path><path d=\"M6 8h2\"></path><path d=\"M6 12h2\"></path><path d=\"M16 8h2\"></path><path d=\"M16 12h2\"></path></svg>",
        "name": "Folder 8",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": false,
        "allowed_users": [
            5
        ],
        "created_by": 5
    },
    {
        "id": 86,
        "description": null,
        "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"24\" height=\"24\" viewBox=\"0 0 24 24\" fill=\"none\" stroke=\"currentColor\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\" class=\"lucide lucide-book-open-text\"><path d=\"M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z\"></path><path d=\"M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z\"></path><path d=\"M6 8h2\"></path><path d=\"M6 12h2\"></path><path d=\"M16 8h2\"></path><path d=\"M16 12h2\"></path></svg>",
        "name": "Folder 6",
        "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
        "default": false,
        "allowed_users": [
            5,
            34,
            35
        ],
        "created_by": 34
    }
]
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout
- **404** - Not Found

## Create a new folder

### HTTP Request

```http
POST /api/files/folders/{project_id}
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "name": "folder14",
    "description": "This is a important folder",
    "icon": "swig",
    "allowed_users": [] //id of users (can update later with emial id of users in update folder)
}
```

### Response Body

```json
{
    "id": 97,
    "description": "This is a important folder",
    "icon": "swig",
    "name": "folder14",
    "project": "5700ac35-1afe-4af9-ac1a-9c1df86c4cde",
    "default": false,
    "files": [],
    "allowed_users": [
        5
    ],
    "created_by": 5
}
```

### Response Status

- **201** - Created
- **400** - Bad Request
- **401** - Unauthorized
- **403** - Forbidden
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

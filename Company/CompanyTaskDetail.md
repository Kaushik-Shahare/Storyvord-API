# Client - Company Task Detail

## Get Task Detail

### HTTP Request

```http
GET /api/company/tasks/:id/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
    "id": 1,
    "created_by": {
        "id": 5,
        "username": null,
        "email": "client12345@gmail.com",
        "first_name": "",
        "last_name": ""
    },
    "completed": true,
    "completion_requested": false,
    "title": "Design new company logo and Design",
    "description": "Create a Figma of each layout page.",
    "due_date": "2024-09-15",
    "created_at": "2024-08-23T14:40:23.235940Z",
    "updated_at": "2024-08-23T14:48:12.288203Z",
    "assigned_to": 34,
    "requester": null
}
```

## Update Task Detail

### HTTP Request

```http
PUT /api/company/tasks/:id/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
  "title": "Design new company logo",
  "description": "Create a modern and professional logo for the company that aligns with our brand values.",
  "due_date": "2024-09-15"
}
```

### Response Body

```json
{
    "id": 1,
    "created_by": {
        "id": 5,
        "username": null,
        "email": "client12345@gmail.com",
        "first_name": "",
        "last_name": ""
    },
    "completed": true,
    "completion_requested": false,
    "title": "Design new company logo and Design",
    "description": "Create a Figma of each layout page.",
    "due_date": "2024-09-15",
    "created_at": "2024-08-23T14:40:23.235940Z",
    "updated_at": "2024-08-25T06:41:29.429115Z",
    "assigned_to": 34,
    "requester": null
}
```

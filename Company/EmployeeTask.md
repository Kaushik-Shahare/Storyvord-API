# Company - Employee Task

## Get Employee Task List

Get all tasks assigned to the employee.

### HTTP Request

```http
GET api/company/employee/tasks/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 2,
        "created_by": {
            "id": 5,
            "username": null,
            "email": "client12345@gmail.com",
            "first_name": "",
            "last_name": ""
        },
        "completed": false,
        "completion_requested": false,
        "title": "Design new company logo",
        "description": "Create a modern and professional logo for the company that aligns with our brand values.",
        "due_date": "2024-09-15",
        "created_at": "2024-08-25T06:35:35.560761Z",
        "updated_at": "2024-08-25T06:35:35.560783Z",
        "assigned_to": 34,
        "requester": null
    },
    {
        "id": 3,
        "created_by": {
            "id": 5,
            "username": null,
            "email": "client12345@gmail.com",
            "first_name": "",
            "last_name": ""
        },
        "completed": false,
        "completion_requested": false,
        "title": "Design new company logo",
        "description": "Create a modern and professional logo for the company that aligns with our brand values.",
        "due_date": "2024-09-15",
        "created_at": "2024-08-25T06:40:47.786446Z",
        "updated_at": "2024-08-25T06:40:47.786461Z",
        "assigned_to": 34,
        "requester": null
    },
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
        "updated_at": "2024-08-25T06:48:29.671672Z",
        "assigned_to": 34,
        "requester": null
    }
]

```

## Get Employee Task Detail

Get the details of a specific task assigned to the employee.

### HTTP Request

```http
GET /api/company/employee/tasks/:id/
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
    "updated_at": "2024-08-25T06:48:29.671672Z",
    "assigned_to": 34,
    "requester": null
}
```

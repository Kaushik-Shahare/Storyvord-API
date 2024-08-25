# Company - Request & Approval Task

## Request Task Completion

Request the completion of a task from the assigned user.

### HTTP Request

```http
POST /api/company/tasks/:id/request-completion/
```

### Request Headers

- **Authorization** - Bearer token

## Get Task Completion Requests List

Get all task completion requests for the client.

### HTTP Request

```http
GET /api/company/tasks/pending-approvals/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 1,
        "created_by": {
            "id": 5,
            "username": null,
            "email": "client12345@gmail.com",
            "first_name": "",
            "last_name": ""
        },
        "completed": false,
        "completion_requested": true,
        "title": "Design new company logo and Design",
        "description": "Create a Figma of each layout page.",
        "due_date": "2024-09-15",
        "created_at": "2024-08-23T14:40:23.235940Z",
        "updated_at": "2024-08-25T06:47:18.424636Z",
        "assigned_to": 34,
        "requester": 34
    }
]
```

## Approve Task Completion

Client approves the completion of a task.

### HTTP Request

```http
POST /api/company/tasks/:id/approve-completion/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

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

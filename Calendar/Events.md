# Calendar - Events

## Get all Events of a Calendar

### HTTP Request

```http
GET /api/calendar/calendars/{project_id}/events/
```

### Request Headers

- Bearer Token

### Response Body

```json
[
    {
        "id": 2,
        "title": "Project Kickoff meeting",
        "description": "Initial meeting to discuss project goals and timelines.",
        "start": "2023-04-01T10:00:00Z",
        "end": "2023-04-01T11:00:00Z",
        "location": "Conference Room A",
        "calendar": 2,
        "participants": [
            1
        ]
    },
    {
        "id": 3,
        "title": "Project Kickoff Meeting",
        "description": "Initial meeting to discuss project goals and timelines.",
        "start": "2023-04-01T10:00:00Z",
        "end": "2023-04-01T11:00:00Z",
        "location": "Conference Room A",
        "calendar": 2,
        "participants": []
    },
    {
        "id": 4,
        "title": "Project Kickoff Meeting",
        "description": "Initial meeting to discuss project goals and timelines.",
        "start": "2023-04-01T10:00:00Z",
        "end": "2023-04-01T11:00:00Z",
        "location": "Conference Room B",
        "calendar": 2,
        "participants": []
    },
    {
        "id": 5,
        "title": "Project Kickoff Meeting",
        "description": "Initial meeting to discuss project goals and timelines.",
        "start": "2024-04-01T10:00:00Z",
        "end": "2024-04-01T11:00:00Z",
        "location": "Conference Room B",
        "calendar": 2,
        "participants": [
            1
        ]
    },
    {
        "id": 6,
        "title": "Project Kickoff Meeting",
        "description": "Initial meeting to discuss project goals and timelines.",
        "start": "2024-04-01T10:00:00Z",
        "end": "2024-04-01T11:00:00Z",
        "location": "Conference Room B",
        "calendar": 2,
        "participants": []
    },
    {
        "id": 7,
        "title": "Project Kickoff Meeting",
        "description": "Initial meeting to discuss project goals and timelines.",
        "start": "2024-04-01T10:00:00Z",
        "end": "2024-04-01T11:00:00Z",
        "location": "Conference Room B",
        "calendar": 2,
        "participants": []
    }
]
```

### Response Status

- **200** - OK
- **401** - Unauthorized

    ```json
    {
        "detail": "You do not have permission to access this calendar"
    }
    ```

- **404** - Not Found

    ```json
    {
        "detail": "Not found."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Create Event

### HTTP Request

```http
POST /api/calendar/calendars/{project_id}/events/
```

### Request Headers

- Bearer Token

### Request Body

```json
{
    "title": "Project Kickoff Meeting",
    "description": "Initial meeting to discuss project goals and timelines.",
    "start": "2024-04-01T10:00:00Z",
    "end": "2024-04-01T11:00:00Z",
    "location": "Conference Room B",
    "participants": [1, 2, 3]
}
```

### Response Body

```json
{
    "id": 8,
    "title": "Project Kickoff Meeting",
    "description": "Initial meeting to discuss project goals and timelines.",
    "start": "2024-04-01T10:00:00Z",
    "end": "2024-04-01T11:00:00Z",
    "location": "Conference Room B",
    "calendar": 2,
    "participants": [1, 2, 3]
}
```

### Response Status

- **201** - Created
- **401** - Unauthorized
- **404** - Not Found
- **409** - Conflict
  - Event with the same title and time already exists
- **500** - Internal Server Error
  - User has event at the same time
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Event

### HTTP Request

```http
PUT /api/calendar/calendars/{project_id}/events/{event_id}
```

### Request Headers

- Bearer Token

### Request Body

```json
{
    "title": "Project Kickoff Meeting",
    "description": "Initial meeting to discuss project goals and timelines.",
    "start": "2024-04-01T10:00:00Z",
    "end": "2024-04-01T11:00:00Z",
    "location": "Conference Room B",
    "participants": [1, 2, 3]
}
```

### Response Body

```json
{
    "id": 8,
    "title": "Project Kickoff Meeting",
    "description": "Initial meeting to discuss project goals and timelines.",
    "start": "2024-04-01T10:00:00Z",
    "end": "2024-04-01T11:00:00Z",
    "location": "Conference Room B",
    "calendar": 2,
    "participants": [1, 2, 3]
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **500** - Internal Server Error
  - User has event at the same time
- **503** - Service Unavailable
- **504** - Gateway Timeout
- **404** - Not Found
- **409** - Conflict
  - Event with the same title and time already exists

## Delete Event

### HTTP Request

```http
DELETE /api/calendar/calendars/{project_id}/events/{event_id}
```

### Request Headers

- Bearer Token

### Response Status

- **204** - No Content
- **401** - Unauthorized
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

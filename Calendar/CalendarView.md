# Calendar View

## Get List of all Calendar Events and Project

### HTTP Request

```http
GET /api/calendar/calendars/
```

### Request Headers

- Bearer Token

### Response Body

```json
[
    {
        "id": 2,
        "events": [
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
        ],
        "name": "New Project Calendar",
        "project": "46a596bf-f5eb-4b02-a35d-dcf782ce59e3"
    },
    {
        "id": 3,
        "events": [],
        "name": "New Project Calendar",
        "project": "b35e4cfe-6723-45ec-9c94-48e360f48e3c"
    },
    {
        "id": 4,
        "events": [],
        "name": "New Project Calendar",
        "project": "f03d715c-6ead-4890-923c-f6f5b11a6d27"
    },
    {
        "id": 5,
        "events": [],
        "name": "New Project Calendar",
        "project": "73cef8e5-c37c-4ae6-967d-3c7814a2fffa"
    },
    {
        "id": 6,
        "events": [],
        "name": "New Project 1 Calendar",
        "project": "3362a725-ca3c-4499-9f58-a798b34d9926"
    }
]
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

### Issues

- We get all calanders of projects where crew member is not a participant. We should only get the calanders of projects where crew member is a participant.

## Get Calendar Details

### HTTP Request

```http
GET /api/calendar/calendars/{project_id}/
```

### Request Headers

- Bearer Token

### Response Body

```json
{
    "id": 2,
    "events": [
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
    ],
    "name": "New Project Calendar",
    "project": "46a596bf-f5eb-4b02-a35d-dcf782ce59e3"
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

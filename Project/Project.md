# Project

## Get all projects

### HTTP Request

```http
GET /api/project/projects/
```

### Request Headers

- Bearer Token

### Response Body

```json
[
  {
    "project_id": "bb77ba32-5b8e-4b7f-8651-2dfc0dd6a6d4",
    "location_details": [
      {
        "id": 1,
        "location": "Location 1",
        "start_date": "2024-07-01",
        "end_date": "2024-07-05",
        "mode_of_shooting": "Mode 1",
        "permits": true
      },
      {
        "id": 2,
        "location": "Location 2",
        "start_date": "2024-07-10",
        "end_date": "2024-07-15",
        "mode_of_shooting": "Mode 2",
        "permits": false
      }
    ],
    "selected_crew": [],
    "equipment": [],
    "uploaded_document": null,
    "name": "New Project 1",
    "brief": "Brief description of the project",
    "additional_details": "Additional details about the project",
    "budget_currency": "$",
    "budget_amount": "100000.00",
    "content_type": "Film",
    "status": "PLANNING",
    "created_at": "2024-07-26T03:08:49.262857Z",
    "updated_at": "2024-07-26T03:08:49.262895Z",
    "crew_profiles": []
  }
]
```

### Response Status

- **200: OK**
- **401: Unauthorized**

  - If the token is invalid
  - If the token is expired

    - ```json
      {
        "detail": "Given token not valid for any token type"
      }
      ```

- **500: Internal Server Error**
- 503: Service Unavailable
- 504: Gateway Timeout
- 507: Insufficient Storage

## Create a project

### HTTP Request

```http
POST /api/project/projects/
```

### Request Headers

- Bearer Token

### Request Body

```json
{
  "name": "New Project 1",
  "brief": "Brief description of the project",
  "additional_details": "Additional details about the project",
  "budget_currency": "$",
  "budget_amount": 100000.0,
  "content_type": "Film",
  "selected_crew": [],
  "equipment": [],
  "location_details": [
    {
      "location": "Location 1",
      "start_date": "2024-07-01",
      "end_date": "2024-07-05",
      "mode_of_shooting": "Mode 1",
      "permits": true
    },
    {
      "location": "Location 2",
      "start_date": "2024-07-10",
      "end_date": "2024-07-15",
      "mode_of_shooting": "Mode 2",
      "permits": false
    }
  ],
  "status": "PLANNING",
  "user": 2
}
```

### Response Body

```json
{
  "project_id": "bb77ba32-5b8e-4b7f-8651-2dfc0dd6a6d4",
  "location_details": [
    {
      "id": 1,
      "location": "Location 1",
      "start_date": "2024-07-01",
      "end_date": "2024-07-05",
      "mode_of_shooting": "Mode 1",
      "permits": true
    },
    {
      "id": 2,
      "location": "Location 2",
      "start_date": "2024-07-10",
      "end_date": "2024-07-15",
      "mode_of_shooting": "Mode 2",
      "permits": false
    }
  ],
  "selected_crew": [],
  "equipment": [],
  "uploaded_document": null,
  "name": "New Project 1",
  "brief": "Brief description of the project",
  "additional_details": "Additional details about the project",
  "budget_currency": "$",
  "budget_amount": "100000.00",
  "content_type": "Film",
  "status": "PLANNING",
  "created_at": "2024-07-26T03:08:49.262857Z",
  "updated_at": "2024-07-26T03:08:49.262895Z",
  "crew_profiles": []
}
```

### Response Status

- **201: Created**
- **400: Bad Request**

  - If the request body is invalid

    - ```json
      {
        "FIELD_NAME": "This field is required."
      }
      ```

- **500: Internal Server Error**
- 503: Service Unavailable
- 504: Gateway Timeout
- 507: Insufficient Storage

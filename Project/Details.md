# Project - Details

## Get Project Details

### HTTP Request

```http
GET /api/project/projects/{project_id}/
```

### Request Headers

- Bearer Token

### Response Body

```json
{
  "project_id": "bc07cc62-035a-4f1d-be7b-dc6287487093",
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
  "created_at": "2024-07-26T03:49:22.542349Z",
  "updated_at": "2024-07-26T03:49:22.542378Z",
  "crew_profiles": []
}
```

### Response Status

- **200: OK**
- **401: Unauthorized**

  - If the user is not authenticated

  ```json
  {
    "detail": "Authentication credentials were not provided."
  }
  ```

  - If the user is not authorized to view the project

  ```json
  {
    "detail": "You do not have permission to perform this action."
  }
  ```

- **404: Not Found**

  - If the project does not exist

    - ```json
      {
        "detail": "Not found."
      }
      ```

## Update Project Details

### HTTP Request

```http
PUT /api/project/projects/{project_id}/
```

### Request Headers

- Bearer Token

### Request Body

- Field you what to update.

#### Example

### Request Body

```json
{
  "user": 1,
  "location_details": [
    {
      "id": 1,
      "location": "Location 1",
      "start_date": "2024-07-01",
      "end_date": "2024-08-05",
      "mode_of_shooting": "Mode 1",
      "permits": true
    },
    {
      "id": 2,
      "location": "Location 2",
      "start_date": "2024-07-10",
      "end_date": "2024-08-15",
      "mode_of_shooting": "Mode 2",
      "permits": false
    }
  ]
}
```

### Response Body

```json
{
  "project_id": "bc07cc62-035a-4f1d-be7b-dc6287487093",
  "location_details": [
    {
      "id": 3,
      "location": "Location 1",
      "start_date": "2024-07-01",
      "end_date": "2024-08-05",
      "mode_of_shooting": "Mode 1",
      "permits": true
    },
    {
      "id": 4,
      "location": "Location 2",
      "start_date": "2024-07-10",
      "end_date": "2024-08-15",
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
  "created_at": "2024-07-26T03:49:22.542349Z",
  "updated_at": "2024-07-26T07:53:58.886851Z",
  "crew_profiles": []
}
```

### Response Status

- **200: OK**
- **401: Unauthorized**

  - If the user is not authenticated

  ```json
  {
    "detail": "Authentication credentials were not provided."
  }
  ```

  - If the user is not authorized to update the project

  ```json
  {
    "detail": "You do not have permission to perform this action."
  }
  ```

- **404: Not Found**

  - If the project does not exist

  ```json
  {
    "detail": "Not found."
  }
  ```

## Delete Project

### HTTP Request

```http
DELETE /api/project/projects/{project_id}/
```

### Request Headers

- Bearer Token

### Response Status

- **204: No Content**
  - Successful deletion
- **401: Unauthorized**

  - If the user is not authenticated

  ```json
  {
    "detail": "Authentication credentials were not provided."
  }
  ```

  - If the user is not authorized to delete the project

  ```json
  {
    "detail": "You do not have permission to perform this action."
  }
  ```

- **404: Not Found**

  - If the project does not exist

  ```json
  {
    "detail": "Project not found."
  }
  ```

- **500: Internal Server Error**
- 503: Service Unavailable
- 504: Gateway Timeout

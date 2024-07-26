# Project - Onboarding requests

## Send Onboarding Request

### HTTP Request

```http
POST /api/project/onboard-requests/send/
```

### Request Headers

- Bearer Token

### Request Body

```json
{
  "project_id": "46a596bf-f5eb-4b02-a35d-dcf782ce59e3",
  "user_id": 1
}
```

### Response Body

```json
{
  "id": 3,
  "project": "46a596bf-f5eb-4b02-a35d-dcf782ce59e3",
  "user": 1,
  "status": "pending",
  "created_at": "2024-07-26T10:41:19.448138Z",
  "updated_at": "2024-07-26T10:41:19.448181Z"
}
```

### Response Status

- **201: Created**
- **400: Bad Request**

  - If the request body is invalid

  ```json
  {
    "error": "Invalid project or user ID."
  }
  ```

- **401: Unauthorized**

  - If the user is not authenticated

  ```json
  {
    "detail": "Authentication credentials were not provided."
  }
  ```

  - If the user is not authorized to send onboarding request

  ```json
  {
    "detail": "You do not have permission to perform this action."
  }
  ```

  - If the user is not authorized to view the project

  ```json
  {
    "detail": "You do not have permission to perform this action."
  }
  ```

  - If the user is not authorized to view the user

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

  - If the user does not exist

  ```json
  {
    "detail": "Not found."
  }
  ```

- **500: Internal Server Error**
- 503: Service Unavailable
- 504: Gateway Timeout

### Issues

- Same user can send multiple requests for the same project.

## Update Onboarding Request

### HTTP Request

```http
PATCH /api/project/onboard-requests/{onboard_request_id}/update/
```

### Request Headers

- Bearer Token

### Request Body

```json
{
  "status": "accepted"
}
```

### Response Body

```json
{
  "id": 3,
  "project": "46a596bf-f5eb-4b02-a35d-dcf782ce59e3",
  "user": 1,
  "status": "accepted",
  "created_at": "2024-07-26T10:41:19.448138Z",
  "updated_at": "2024-07-26T10:41:19.448181Z"
}
```

### Response Status

- **200: OK**
- **400: Bad Request**

  - If the request body is invalid
  - status is not valid

  ```json
  {
    "error": "Invalid status."
  }
  ```

- **401: Unauthorized**

  - If the user is not authenticated

  ```json
  {
    "detail": "Authentication credentials were not provided."
  }
  ```

  - If the user is not authorized to update onboarding request

  ```json
  {
    "detail": "You do not have permission to perform this action."
  }
  ```

- **404: Not Found**

  - If the onboarding request does not exist

  ```json
  {
    "detail": "Not found."
  }
  ```

- **500: Internal Server Error**
- 503: Service Unavailable
- 504: Gateway Timeout

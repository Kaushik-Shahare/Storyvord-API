# Crew

## Get Crew

### HTTP Request

```http
GET /api/crew/crew-profile/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
  "id": 20,
  "name": null,
  "phone": null,
  "image": null,
  "location": null,
  "languages": null,
  "job_title": null,
  "bio": null,
  "experience": null,
  "skills": null,
  "technicalProficiencies": null,
  "specializations": null,
  "drive": false,
  "user": 31
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Crew

### HTTP Request

```http
PUT /api/crew/crew-profile/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
  "name": "string",
  "phone": "string",
  "image": "string",
  "location": "string",
  "languages": "string",
  "job_title": "string",
  "bio": "string",
  "experience": "string",
  "skills": "string",
  "technicalProficiencies": "string",
  "specializations": "string",
  "drive": true
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

# Crew - Education Details

## Get Crew Education Details

### HTTP Request

```http
GET /api/crew/crew-education/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
    "id": 7,
    "academicQualifications": null,
    "professionalCourses": null,
    "workshopsAttended": null,
    "crew": 22
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

    ```json
    {
    "detail": "No CrewEducation matches the given query."
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Crew Education

### HTTP Request

```http
PUT /api/crew/crew-education/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "academicQualifications": "B.Tech",
    "professionalCourses": "Python",
    "workshopsAttended": "Machine Learning"
}
```

### Response Body

```json
{
    "id": 7,
    "academicQualifications": "B.Tech",
    "professionalCourses": "Python",
    "workshopsAttended": "Machine Learning",
    "crew": 22
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

### Issues

- crew field is editable which should not be the case. It should be read-only.

## Delete Crew Education

### HTTP Request

```http
DELETE /api/crew/crew-education/{id}/
```

### Request Headers

- **Authorization** - Bearer token

### Response Status

- **204** - No Content
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

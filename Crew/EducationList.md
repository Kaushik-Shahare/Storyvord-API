# Crew - Education List

## Get Crew Education List

### HTTP Request

```http
GET /api/crew/crew-education/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "id": 7,
        "academicQualifications": null,
        "professionalCourses": null,
        "workshopsAttended": null,
        "crew": 22
    },
    {
        "id": 8,
        "academicQualifications": null,
        "professionalCourses": null,
        "workshopsAttended": null,
        "crew": 22
    }
]
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

## Create Crew Education

### HTTP Request

```http
POST /api/crew/crew-education/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
    "academicQualifications": "B.Tech",
    "professionalCourses": "Java",
    "workshopsAttended": "Workshop",
    "crew": 22
}
```

### Response Body

```json
{
    "id": 8,
    "academicQualifications": "B.Tech",
    "professionalCourses": "Java",
    "workshopsAttended": "Workshop",
    "crew": 22
}
```

### Response Status

- **201** - Created
- **400** - Bad Request
  - Invalid data

    ```json
    {
    "crew": [
        "Incorrect type. Expected pk value, received list."
    ]
    }
    ```

  - Missing data

    ```json
    {
    "crew": [
        "This field is required."
    ]
    }
    ```

- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a crew
- **404** - Not Found

    ```json
    {
    "crew": [
        "Invalid pk \"222\" - object does not exist."
    ]
    }
    ```

- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

### Issues

- Does not create a new education record for the signed in crew member.
- Anyone can create an education record for any crew member.

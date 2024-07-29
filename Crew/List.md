# Crew - All crew

## List Crew

### HTTP Request

```http
GET /api/crew/crew-list
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
[
    {
        "crew_profile": {
            "id": 1,
            "name": "Kaushik",
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
            "user": 1
        },
        "crew_credits": [
            {
                "id": 2,
                "title": "Crew Title",
                "year": "2 years",
                "role": "xyz",
                "production": "abc",
                "client": null,
                "type_of_content": "Film",
                "tags": null,
                "crew": 1
            },
            {
                "id": 3,
                "title": "Crew Title",
                "year": "2 years",
                "role": "xyz",
                "production": "abc",
                "client": null,
                "type_of_content": "Film",
                "tags": null,
                "crew": 1
            },
            {
                "id": 4,
                "title": "Crew Title",
                "year": "2 years",
                "role": "xyz",
                "production": "abc",
                "client": null,
                "type_of_content": "Film",
                "tags": null,
                "crew": 1
            }
        ],
        "crew_education": [
            {
                "id": 2,
                "academicQualifications": "Btech CSE",
                "professionalCourses": null,
                "workshopsAttended": null,
                "crew": 1
            },
            {
                "id": 3,
                "academicQualifications": null,
                "professionalCourses": null,
                "workshopsAttended": null,
                "crew": 1
            },
            {
                "id": 4,
                "academicQualifications": null,
                "professionalCourses": null,
                "workshopsAttended": null,
                "crew": 1
            },
            {
                "id": 5,
                "academicQualifications": null,
                "professionalCourses": null,
                "workshopsAttended": null,
                "crew": 1
            },
            {
                "id": 6,
                "academicQualifications": null,
                "professionalCourses": null,
                "workshopsAttended": null,
                "crew": 1
            }
        ],
        "crew_rate": [
            {
                "id": 2,
                "standardRate": null,
                "negotiation": false,
                "crew": 1
            },
            {
                "id": 3,
                "standardRate": null,
                "negotiation": true,
                "crew": 1
            },
            {
                "id": 4,
                "standardRate": null,
                "negotiation": true,
                "crew": 1
            }
        ],
        "endorsement_from_peers_data": [
            {
                "id": 1,
                "text": "text",
                "givenBy": "givenBy",
                "crew": 1
            }
        ],
        "social_links": [
            {
                "id": 1,
                "link": "https://youtube.com",
                "crew": 1
            }
        ]
    },
    {
        "crew_profile": {
            "id": 2,
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
            "user": 2
        },
        "crew_credits": [
            {
                "id": 5,
                "title": "Crew Title",
                "year": "2 years",
                "role": "xyz",
                "production": "abc",
                "client": null,
                "type_of_content": "Film",
                "tags": null,
                "crew": 2
            }
        ],
        "crew_education": [],
        "crew_rate": [
            {
                "id": 5,
                "standardRate": null,
                "negotiation": false,
                "crew": 2
            }
        ],
        "endorsement_from_peers_data": [],
        "social_links": []
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
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

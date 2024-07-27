# Client

## Get Client

### HTTP Request

```http
GET /api/client/profile/detail/
```

### Request Headers

- **Authorization** - Bearer token

### Response Body

```json
{
  "firstName": null,
  "lastName": null,
  "formalName": null,
  "role": null,
  "description": null,
  "address": null,
  "countryName": null,
  "locality": null,
  "personalWebsite": null
}
```

### Response Status

- **200** - OK
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a client
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Update Client

### HTTP Request

```http
PUT /api/client/profile/detail/
```

### Request Headers

- **Authorization** - Bearer token

### Request Body

```json
{
  "firstName": "string",
  "lastName": "string",
  "formalName": "string",
  "role": "string",
  "description": "string",
  "address": "string",
  "countryName": "string",
  "locality": "string",
  "personalWebsite": "string"
}
```

### Response Body

- Client after update

```json
{
  "firstName": "string",
  "lastName": "string",
  "formalName": "string",
  "role": "string",
  "description": "string",
  "address": "string",
  "countryName": "string",
  "locality": "string",
  "personalWebsite": "string"
}
```

### Response Status

- **200** - OK
- **400** - Bad Request
  - Invalid request body
  - Invalid request parameters
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a client
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

## Delete Client

### HTTP Request

```http
DELETE /api/client/profile/detail/
```

### Request Headers

- **Authorization** - Bearer token

### Response Status

- **200** - OK
- **401** - Unauthorized
  - User is not logged in
  - Token is invalid
- **403** - Forbidden
  - User is not a client
- **404** - Not Found
- **500** - Internal Server Error
- **503** - Service Unavailable
- **504** - Gateway Timeout

```

```

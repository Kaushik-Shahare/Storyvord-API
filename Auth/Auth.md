# Authentication

## Sign ups

### HTTP Request

```http
POST /auth/users
```

### Request Body

```json
{
  "user_type": "client",
  "email": "qxhd0dhl2t@hellomailo.net",
  "firstName": "Kaushik",
  "password": "1231231234abcabcabcd"
}
```

### Response Body

```json
{
  "user_type": "client",
  "email": "qxhd0dhl2z@hellomailo.net",
  "id": 27
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

- **409: Conflict**

  - If the email is already in use

    - ```json
      {
        "email": "user with this email already exists."
      }
      ```

- **500: Internal Server Error**
- 503: Service Unavailable
- 504: Gateway Timeout
- 507: Insufficient Storage

## Sign in

### HTTP Request

```http
POST /auth/jwt/create/
```

### Request Body

```json
{
  "email": "qxhd0dhl2t@hellomailo.net",
  "password": "1231231234abcabcabcd"
}
```

### Response Body

```json
{
  "refresh": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTcyMjEzNTQ1OSwiaWF0IjoxNzIxOTYyNjU5LCJqdGkiOiI3MGJlZTJlOWRlMzQ0NTdlYmM4YzNkMjRlZDVmMTQ2ZiIsInVzZXJfaWQiOjI2fQ.XKpN9UD7rQZ0v-I6nGMXPfgssWofkrvy-ukiKWVhrtU",
  "access": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNzIyMDQ5MDU5LCJpYXQiOjE3MjE5NjI2NTksImp0aSI6IjhjOThmM2U4MDg1ODRkNGZiNjdkYjAyMGQ0YzRkNmZhIiwidXNlcl9pZCI6MjZ9.QLjKeTaaEivYrOTw7V_zgRJTOSRkTrN-nEfWmLrSqeA"
}
```

**Note:** The `access` token is used to authenticate further requests.

### Response Status

- **200: OK**
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

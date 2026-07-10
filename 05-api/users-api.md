# Users API

## Base URL

```
http://localhost:3000
```

---

## GET /users

Returns all users.

### Response

**Status**

```
200 OK
```

**Example**

```json
[
  {
    "id": "uuid",
    "firstName": "Parthib",
    "lastName": "Datta",
    "email": "parthib@test.com"
  }
]
```

---

## GET /users/:id

Returns a single user.

### Success

**Status**

```
200 OK
```

**Example**

```json
{
  "id": "be9d1ad9-760d-4e8b-ab86-f87b17f2ad49",
  "firstName": "Parthib",
  "lastName": "Datta",
  "email": "parthib@test.com",
  "phone": "01888888888",
  "role": "CUSTOMER",
  "status": "ACTIVE"
}
```

### Not Found

```
404 Not Found
```

```json
{
  "message": "User not found",
  "error": "Not Found",
  "statusCode": 404
}
```

---

## POST /users

Creates a new user.

### Request

```json
{
  "firstName": "Parthib",
  "lastName": "Datta",
  "email": "parthib@test.com",
  "phone": "01700000000",
  "passwordHash": "temporary_hash"
}
```

### Success

```
201 Created
```

### Duplicate Email

```
409 Conflict
```

```json
{
  "message": "Email already exists",
  "error": "Conflict",
  "statusCode": 409
}
```

---

## PATCH /users/:id

Updates an existing user.

### Request

```json
{
  "phone": "01888888888"
}
```

### Success

```
200 OK
```

Returns the updated user.

### Not Found

```
404 Not Found
```

```json
{
  "message": "User not found",
  "error": "Not Found",
  "statusCode": 404
}
```
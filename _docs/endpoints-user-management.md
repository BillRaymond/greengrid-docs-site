---
layout: page
title: Endpoints User Management
permalink: /docs/endpoints-user-management/
sort: 9
---

### Overview

User management endpoints let you create, update, delete, and retrieve users in your GreenGrid-integrated application. These endpoints are essential for identity mapping, role-based access, and onboarding automation.

### Base URL

```
https://api.greengrid.com/v1/users
```

### Supported Methods

| Method | Description                 |
|--------|-----------------------------|
| GET    | Retrieve user information   |
| POST   | Create a new user           |
| PATCH  | Update user data            |
| DELETE | Delete a user account       |

---

### GET /users/{user_id}

Retrieve profile information for a specific user.

#### Sample Request

```
GET /v1/users/b43d-82ff
Authorization: Bearer YOUR_API_KEY
```

#### Sample Response

```json
{
  "user_id": "b43d-82ff",
  "email": "user@example.com",
  "role": "homeowner",
  "created_at": "2024-09-12T17:03:00Z"
}
```

---

### POST /users

Create a new GreenGrid user.

#### Request Body

```json
{
  "email": "newuser@example.com",
  "role": "homeowner"
}
```

#### Sample Response

```json
{
  "user_id": "u122-93ca",
  "status": "created"
}
```

---

### PATCH /users/{user_id}

Update user attributes like role or contact information.

```json
{
  "role": "utility"
}
```

---

### DELETE /users/{user_id}

Remove a user account and associated data.

```json
{
  "message": "User deleted successfully"
}
```

---

### Best Practices

- Validate email formats on creation.
- Use roles (`homeowner`, `utility`, `admin`) to define access scope.
- Use soft deletion for auditability in enterprise applications.

---

For access management or account recovery, see [Authentication Guide](./authentication-guide.md).

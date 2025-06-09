---
layout: page
title: Error codes and responses
permalink: /docs/error-codes-responses/
sort: 5
---
GreenGrid API uses standard HTTP status codes to indicate the success or failure of your requests. This page will help you understand common error responses and how to fix them.

### Response Format

All errors follow a consistent JSON structure:

```json
{
  "error": "Description of the issue",
  "status": 4XX
}
```

### Common HTTP Status Codes

| Code | Message             | Meaning                                                      | What to Do                                  |
|------|---------------------|--------------------------------------------------------------|----------------------------------------------|
| 200  | OK                  | Request succeeded                                            | No action needed                             |
| 201  | Created             | Resource successfully created                                | Confirm your POST payload is correct         |
| 400  | Bad Request         | Request could not be understood                             | Check syntax, parameters, or JSON formatting |
| 401  | Unauthorized        | Missing or invalid API key                                  | Re-authenticate and ensure proper formatting |
| 403  | Forbidden           | API key lacks necessary permissions                         | Upgrade access or request new permissions    |
| 404  | Not Found           | Requested resource does not exist                           | Double-check the endpoint or resource ID     |
| 409  | Conflict            | Request conflicts with existing resource state              | Resolve conflicts before retrying            |
| 422  | Unprocessable Entity| Validation failed (e.g., incorrect date format)             | Review input and try again                   |
| 429  | Too Many Requests   | Rate limit exceeded                                          | Wait and retry using exponential backoff     |
| 500  | Internal Server Error | Unexpected error on GreenGrid's side                      | Retry later or report the issue              |
| 503  | Service Unavailable | API is temporarily offline or overloaded                    | Wait and try again later                     |

### Example: Invalid Token

#### Request

```
GET /v1/user-profile HTTP/1.1
Authorization: Bearer INVALID_TOKEN
```

#### Response

```json
{
  "error": "Unauthorized",
  "status": 401
}
```

### Debugging Tips

- Use tools like Postman to inspect headers and responses.
- Double-check token and payload formatting.
- Refer to the [Authentication Guide](./authentication-guide.md) for correct usage.
- If the problem persists, log the full request/response for analysis.

---

Need help with an error you're seeing? [Reach out to Support](https://support.greengrid.com) with your request ID and timestamp.

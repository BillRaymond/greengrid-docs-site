---
layout: page
title: Webhooks And Event Subscriptions
permalink: /docs/webhooks-event-subscriptions/
sort: 10
---

### Overview

Webhooks let your application receive real-time data from GreenGrid when specific events occur. This is useful for syncing usage data, triggering alerts, or logging activity as it happens.

### Base URL

```
https://api.greengrid.com/v1/webhooks
```

### Supported Methods

| Method | Description                       |
|--------|-----------------------------------|
| POST   | Register a new webhook            |
| GET    | Retrieve current subscriptions    |
| DELETE | Remove a webhook subscription     |

---

### Available Events

| Event Name       | Description                                |
|------------------|--------------------------------------------|
| usage.updated    | New usage data is available                |
| alert.triggered  | A user-defined alert was triggered         |
| device.connected | A device was successfully paired           |
| user.created     | A new user account was registered          |

---

### POST /webhooks

Register a webhook to subscribe to one or more events.

#### Request Body

```json
{
  "event": "usage.updated",
  "url": "https://yourapp.com/hooks/greengrid",
  "auth_token": "secure-token-abc123"
}
```

#### Sample Response

```json
{
  "webhook_id": "whk-998ac",
  "status": "active"
}
```

---

### GET /webhooks

Retrieve a list of active webhook subscriptions.

```json
[
  {
    "webhook_id": "whk-998ac",
    "event": "usage.updated",
    "url": "https://yourapp.com/hooks/greengrid"
  }
]
```

---

### DELETE /webhooks/{webhook_id}

Unsubscribe from a webhook.

```json
{
  "message": "Webhook removed"
}
```

---

### Retry Behavior

- GreenGrid retries failed deliveries up to 5 times using exponential backoff.
- If a webhook consistently fails, it will be paused.
- Ensure your endpoint responds with HTTP `2xx` status within 5 seconds.

---

Need more control or analytics on delivery? Check [Notification History](./user-notification-history.md).

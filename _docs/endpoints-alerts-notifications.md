---
layout: page
title: Endpoints Alerts And Notifications
permalink: /docs/endpoints-alerts-notifications/
sort: 8
---
### Overview

These endpoints allow you to manage EnergyPulse alerts and configure how users are notified about significant energy usage events. Use them to enable real-time push notifications, SMS, or webhook triggers.

### Base URL

```
https://api.greengrid.com/v1/alerts
```

### Supported Methods

| Method | Description                          |
|--------|--------------------------------------|
| GET    | List all alerts for a user           |
| POST   | Create a new alert                   |
| PATCH  | Update an existing alert             |
| DELETE | Remove an alert                      |

---

### GET /alerts

Retrieve all alerts configured for a specific user.

#### Request

```
GET /v1/alerts?user_id=b43d-82ff
Authorization: Bearer YOUR_API_KEY
```

#### Sample Response

```json
[
  {
    "alert_id": "alr-001",
    "type": "peak_usage",
    "threshold_kwh": 15,
    "delivery": "sms"
  }
]
```

---

### POST /alerts

Create a new usage alert.

#### Request Body

```json
{
  "user_id": "b43d-82ff",
  "type": "peak_usage",
  "threshold_kwh": 20,
  "delivery": "webhook"
}
```

#### Sample Response

```json
{
  "alert_id": "alr-002",
  "status": "active"
}
```

---

### PATCH /alerts/{alert_id}

Modify an existing alert's parameters.

```json
{
  "threshold_kwh": 18,
  "delivery": "email"
}
```

---

### DELETE /alerts/{alert_id}

Delete a user alert.

```json
{
  "message": "Alert removed successfully"
}
```

---

### Webhook Configuration

For alerts delivered via webhook:

- Use `POST` endpoint: `/v1/webhooks`
- Provide a valid HTTPS callback URL
- GreenGrid retries failed calls with exponential backoff

---

Need to audit notification logs or test alert triggers? Visit the [Notification History Page](./user-notification-history.md).

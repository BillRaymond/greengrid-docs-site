---
layout: page
title: Endpoints for Energy Insights
permalink: /docs/endpoints-energy-insights/
sort: 7
---

### Overview

The Energy Insights endpoints allow you to retrieve electricity usage data, compare consumption trends, and monitor peak usage times. These endpoints are ideal for dashboards, billing summaries, and sustainability reporting.

### Base URL

```
https://api.greengrid.com/v1/energy-insights
```

### Supported Methods

| Method | Description                     |
|--------|---------------------------------|
| GET    | Retrieve energy data            |
| POST   | Filter or customize insight reports |

---

### GET /energy-insights

Retrieves daily or monthly usage data for a user.

#### Request

```
GET /v1/energy-insights?start=2025-05-01&end=2025-05-31
Authorization: Bearer YOUR_API_KEY
```

#### Query Parameters

- `start`: Start date in `YYYY-MM-DD` format (required)
- `end`: End date in `YYYY-MM-DD` format (required)
- `group_by`: `day` (default) or `month`

#### Sample Response

```json
{
  "user_id": "b43d-82ff",
  "data": [
    {
      "date": "2025-05-01",
      "kwh_used": 12.4,
      "peak_hour": "19:00"
    },
    {
      "date": "2025-05-02",
      "kwh_used": 10.7,
      "peak_hour": "20:00"
    }
  ]
}
```

---

### POST /energy-insights

Used for advanced filtering or user-specific summaries.

#### Request Body

```json
{
  "user_id": "b43d-82ff",
  "interval": "month",
  "metrics": ["kwh_used", "peak_hour"]
}
```

#### Sample Response

```json
{
  "summary": {
    "total_kwh": 420.5,
    "avg_daily_kwh": 13.6,
    "peak_usage_time": "18:00"
  }
}
```

---

### Use Cases

- Display usage graphs by day or month
- Detect peak demand periods
- Automate usage-based alerts

---

Need deeper visibility or want to segment by device? See [Device Management Endpoints](./endpoints-device-management.md).

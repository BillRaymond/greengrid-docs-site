---
layout: page
title: Data Models
permalink: /docs/data-models/
sort: 6
---
Understanding the structure of data returned by the GreenGrid API helps you build faster and more reliable integrations. This guide outlines key objects, their attributes, and how they relate.

### Common Objects

#### User

Represents a GreenGrid account holder.

```json
{
  "user_id": "b43d-82ff",
  "email": "user@example.com",
  "created_at": "2024-09-12T17:03:00Z",
  "role": "homeowner"
}
```

- `user_id`: Unique identifier for the user
- `email`: User’s registered email address
- `created_at`: ISO timestamp of account creation
- `role`: User role (`homeowner`, `utility`, `admin`)

#### Device

Represents a smart device connected to GreenGrid.

```json
{
  "device_id": "d901-22ac",
  "type": "smart_meter",
  "location": "Main Panel",
  "status": "active"
}
```

- `device_id`: Unique ID of the device
- `type`: Device type (e.g., `smart_meter`, `thermostat`)
- `location`: Physical installation point
- `status`: Current state (`active`, `inactive`, `faulty`)

#### EnergyInsight

Captures time-based energy usage.

```json
{
  "user_id": "b43d-82ff",
  "date": "2025-05-31",
  "kwh_used": 13.2,
  "peak_hour": "18:00"
}
```

- `date`: The calendar date of measurement
- `kwh_used`: Total kilowatt-hours consumed
- `peak_hour`: Hour of highest usage

### Relationships

- A user can have multiple devices.
- Each device reports insights daily.
- EnergyInsight data is tied to both user and device IDs.

### Best Practices

- Use IDs rather than emails to reference users.
- Cache frequent lookups to reduce API calls.
- When storing data, normalize models to improve performance.

---

Want to explore live data? Use the [API Reference](./api-reference.md) or query insights using sample requests in Postman.

---
layout: page
title: Getting started
permalink: /docs/getting-started/
sort: 3
---
Welcome to the GreenGrid API. This guide will help you set up your development environment, make your first request, and understand how to explore the API.

### Who This Is For

Whether you're building an energy dashboard, integrating smart devices, or optimizing usage patterns, this guide is for:

- Developers new to GreenGrid
- Tech teams at utilities and energy startups
- Engineers exploring clean energy integrations

### Prerequisites

Before you begin, make sure you have:

- A GreenGrid developer account ([Sign up here](https://developers.greengrid.com))
- An active API key
- Basic knowledge of HTTP and JSON
- A tool to make requests, like `curl`, Postman, or a REST client

### Set Up Your Environment

We recommend testing requests in a secure, local development environment.

#### Example using `curl` (macOS, Linux)

```
curl -X GET https://api.greengrid.com/v1/energy-insights \
  -H "Authorization: Bearer YOUR_API_KEY"
```

Replace `YOUR_API_KEY` with your actual API key.

### First API Call

Let’s retrieve energy usage data.

#### Endpoint

```
GET /v1/energy-insights
```

#### Sample Response

```json
{
  "user_id": "b43d-82ff",
  "date_range": {
    "start": "2025-05-01",
    "end": "2025-05-31"
  },
  "kwh_used": 420.5,
  "peak_usage_time": "17:00"
}
```

> **Note:** All responses are in UTC unless specified otherwise.

### Explore the API

Once you’ve verified your first request, explore these next steps:

- Read the [Authentication Guide](./authentication-guide.md)
- Review available [Endpoints](./api-reference.md)
- Check [Rate Limits](./rate-limits.md)

### Troubleshooting Tips

- If you receive a 401 error, check that your API key is included and formatted correctly.
- If you get a timeout, verify your internet connection and endpoint URL.
- Always use HTTPS. HTTP requests will be rejected.

---

Still stuck? [Visit the Help Center](https://support.greengrid.com) or reach out to our support team.

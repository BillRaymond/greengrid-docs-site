---
layout: page
title: Rate limits and quotas
permalink: /docs/rate-limits/
sort: 4
---
To ensure consistent performance for all users, GreenGrid enforces rate limits on API usage. This guide explains how rate limits work, what quotas apply, and how to avoid common issues.

### Why Rate Limits Matter

Rate limiting prevents abuse, protects infrastructure, and ensures fair access across the platform. It also encourages efficient API design by discouraging excessive polling or redundant requests.

### Standard Limits

GreenGrid applies different limits depending on the API tier associated with your account.

| Plan Tier     | Requests per Minute | Requests per Day |
|---------------|---------------------|------------------|
| Free          | 30                  | 5,000            |
| Developer     | 60                  | 25,000           |
| Enterprise    | 120                 | 100,000          |

> **Note:** These values are subject to change. Always refer to your Developer Dashboard for real-time usage.

### How Throttling Works

If you exceed your rate limit:

- The request will return a `429 Too Many Requests` status.
- A `Retry-After` header may be included to suggest when to try again.
- Continued abuse may lead to temporary suspension.

#### Sample 429 Response

```json
{
  "error": "Rate limit exceeded",
  "status": 429,
  "retry_after": 30
}
```

### Best Practices to Avoid Throttling

- Use caching for frequently accessed data.
- Batch requests when possible.
- Implement exponential backoff when retrying failed calls.
- Monitor your usage via the [Developer Dashboard](https://developers.greengrid.com/dashboard).

### Monitoring Your Quota

You can track your API usage in real-time.

1. Log in to your Developer Dashboard.
2. Navigate to **Usage & Quotas**.
3. Set up alerts to warn when you're nearing limits.

---

Need higher limits or planning a high-volume integration? [Contact our sales team](https://greengrid.com/contact) to learn about Enterprise plans.

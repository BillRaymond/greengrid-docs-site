---
layout: page
title: Authentication Guide
permalink: /docs/authentication/
sort: 2
---
To keep your data safe and access secure, all GreenGrid API requests must be authenticated. This guide walks you through how to get started.

### Why Authentication Matters

Authentication ensures that only authorized users can access data and perform actions. It protects customer privacy and prevents misuse of energy insights.

### API Key Basics

You need a GreenGrid API key to make authenticated requests.

#### Get Your API Key

1. Log in to your [GreenGrid Developer Dashboard](https://developers.greengrid.com).
2. Go to **API Keys**.
3. Click **Create New Key**.
4. Copy and store your key securely. You won’t be able to view it again.

> **Tip:** Treat your API key like a password. Don’t share it or commit it to public code.

### Making Authenticated Requests

All authenticated requests must include your API key in the `Authorization` header.

#### Example Header

```
GET /v1/energy-insights HTTP/1.1
Host: api.greengrid.com
Authorization: Bearer YOUR_API_KEY
```

Replace `YOUR_API_KEY` with your actual key.

### Token Expiry & Rotation

While API keys do not expire by default, we recommend rotating keys every 90 days for best security practices.

#### Rotate Your API Key

1. Log in to the Developer Dashboard.
2. Revoke the old key.
3. Generate a new key.
4. Update your systems immediately.

### Error Handling

Here are common authentication errors and how to resolve them:

| Status Code | Message              | What to Do                                      |
|-------------|----------------------|--------------------------------------------------|
| 401         | Unauthorized          | Check your API key. Make sure it's valid.        |
| 403         | Forbidden             | Your key may lack the required permissions.      |
| 429         | Too Many Requests     | You've hit your rate limit. Try again later.     |

### Keep It Secure

- Use HTTPS for every request.
- Store keys in server-side environment variables.
- Never expose keys in client-side code.

---

Need help? [Contact Support](https://support.greengrid.com) or view the [API Reference](https://developers.greengrid.com/docs/api-reference).

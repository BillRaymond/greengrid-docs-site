---
layout: page
title: FAQ And Troubleshooting
permalink: /docs/faq-and-troubleshooting/
sort: 13
---

### Overview

This section addresses the most frequently asked questions about using the GreenGrid API and provides troubleshooting tips to help you solve common issues quickly.

---

### Frequently Asked Questions

#### What happens if I lose my API key?

Log in to your [Developer Dashboard](https://developers.greengrid.com), revoke the old key, and generate a new one. Remember to update your integrations with the new key immediately.

#### Can I use the API for commercial applications?

Yes. The API is designed for both personal and commercial projects. For high-volume or enterprise use, contact us for enhanced rate limits and support.

#### Is there a sandbox environment?

Yes. All developer accounts include access to a sandbox mode. Use the base URL `https://sandbox-api.greengrid.com` for testing without affecting live data.

#### What is the data retention policy?

Usage and device data are retained for a minimum of 12 months. You can request data exports or deletions in compliance with privacy regulations.

---

### Troubleshooting Tips

#### 401 Unauthorized

- Ensure your API key is included in the `Authorization` header.
- Double-check that the key hasn’t been revoked or expired.

#### 403 Forbidden

- You may be trying to access a restricted endpoint.
- Check your role and permissions.

#### 404 Not Found

- Confirm the endpoint path and resource ID are correct.
- Some endpoints require query parameters.

#### 429 Too Many Requests

- You’ve hit your rate limit.
- Wait and retry using exponential backoff.

#### 500 Internal Server Error

- The issue is on GreenGrid’s side.
- Retry after a short delay or contact support if it persists.

---

### Get Help

Still stuck? Try the following:

- Visit the [Help Center](https://support.greengrid.com)
- Ask a question in our [Developer Community](https://community.greengrid.com)
- File a support ticket with your request ID and timestamp

---

For release-specific issues, refer to the [Changelog](./changelog.md) to check for recent updates.

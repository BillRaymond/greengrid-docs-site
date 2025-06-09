---
layout: page
title: Changelog
permalink: /docs/changelog/
sort: 14
---

### Overview

The changelog keeps you informed about updates to the GreenGrid API, SDKs, and documentation. Each entry includes version details, release date, highlights, and technical changes.

---

### v1.6.0 – 2025-06-01

**Highlights:**

- New webhook event: `device.connected`
- SDK updates for Python and JavaScript
- Energy insights endpoint now supports `group_by=hour`

**Technical Changes:**

- Added support for hourly aggregation in `/energy-insights`
- Improved error handling for invalid date formats
- Enhanced retry logic for webhook delivery failures

---

### v1.5.2 – 2025-05-10

**Highlights:**

- Performance improvements for device listings
- Minor SDK bug fixes

**Technical Changes:**

- Reduced response time for `/devices`
- Fixed a caching issue in `greengrid-sdk-js`

---

### v1.5.0 – 2025-04-15

**Highlights:**

- New endpoint: `/alerts`
- Notification delivery via email and webhook

**Technical Changes:**

- Introduced alert creation and management
- Added delivery method parameter (`email`, `sms`, `webhook`)

---

### v1.4.0 – 2025-03-01

**Highlights:**

- Major API documentation refresh
- Authentication guide updated with rotation best practices

**Technical Changes:**

- Standardized error response structure across all endpoints
- Deprecated support for XML payloads (JSON only moving forward)

---

Looking for historical changes or archived versions? Contact [Support](https://support.greengrid.com) for access to the full version history.

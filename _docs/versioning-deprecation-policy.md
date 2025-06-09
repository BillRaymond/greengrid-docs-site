---
layout: page
title: Versioning And Deprecation Policy
permalink: /docs/versioning-deprecation-policy/
sort: 12
---

### Overview

GreenGrid uses a clear and predictable versioning policy to help you manage API changes with confidence. This page explains how versions are released, how long they are supported, and what to expect during deprecation.

### Version Format

We use semantic versioning: `v{major}.{minor}.{patch}`

- **Major**: Breaking changes (e.g., `v2.0`)
- **Minor**: Backward-compatible feature updates (e.g., `v1.2`)
- **Patch**: Backward-compatible bug fixes (e.g., `v1.2.1`)

The base API URL includes the major version only:

```
https://api.greengrid.com/v1/
```

---

### Release Schedule

- **Minor and patch updates**: Released monthly as needed
- **Major updates**: Released no more than twice per year
- All new features target the latest major version

---

### Deprecation Policy

When an API version is deprecated:

1. A minimum **6-month notice** is provided.
2. Deprecated versions remain accessible during the grace period.
3. Breaking changes are communicated via:
   - Email alerts
   - Developer Dashboard notifications
   - [Changelog updates](./changelog.md)

---

### Migration Support

We provide migration guides and backwards compatibility flags for most transitions. SDKs and API clients are updated within 2 weeks of each major release.

> **Tip:** Subscribe to our [Developer Newsletter](https://developers.greengrid.com/newsletter) for early access to beta features.

---

Need help upgrading? Our [support team](https://support.greengrid.com) can assist with migration planning or validation.

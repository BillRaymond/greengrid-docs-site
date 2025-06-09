---
layout: page
title: SDKs And Libraries
permalink: /docs/sdks-and-libraries/
sort: 11
---

### Overview

GreenGrid offers SDKs and client libraries to help you integrate faster and reduce boilerplate code. These libraries wrap standard API calls and include built-in error handling, authentication helpers, and response parsing.

### Available SDKs

| Language   | Package Name                | Install Command                          |
|------------|-----------------------------|-------------------------------------------|
| JavaScript | greengrid-sdk-js            | `npm install greengrid-sdk-js`           |
| Python     | greengrid-sdk-python        | `pip install greengrid-sdk-python`       |
| Java       | greengrid-sdk-java          | Available via Maven or Gradle            |
| Ruby       | greengrid-sdk-ruby          | `gem install greengrid-sdk-ruby`         |

---

### Example: JavaScript

#### Setup

```js
import { GreenGridClient } from 'greengrid-sdk-js';

const client = new GreenGridClient({ apiKey: 'YOUR_API_KEY' });
```

#### Fetch Insights

```js
const insights = await client.getEnergyInsights({
  start: '2025-05-01',
  end: '2025-05-31'
});

console.log(insights);
```

---

### Example: Python

#### Setup

```python
from greengrid_sdk import GreenGridClient

client = GreenGridClient(api_key='YOUR_API_KEY')
```

#### Fetch Insights

```python
data = client.get_energy_insights(start='2025-05-01', end='2025-05-31')
print(data)
```

---

### Authentication

All SDKs use the same token-based system. Pass your API key securely during client initialization.

> **Tip:** Never hard-code API keys in your source code. Use environment variables or a secrets manager.

---

### Community and Contributions

We welcome contributions. Visit our [GitHub organization](https://github.com/greengrid) for source code, issue tracking, and contribution guidelines.

---

Looking for integration guides? See our [Getting Started](./getting-started.md) section or explore [Example Projects](https://developers.greengrid.com/examples).

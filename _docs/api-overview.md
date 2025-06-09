---
layout: page
title: API Overview
permalink: /docs/api-overview/
sort: 1
---
## Overview

Welcome to the GreenGrid Energy API. This powerful set of endpoints enables you to seamlessly integrate smart energy data into your apps, dashboards, and systems. Whether you're optimizing household efficiency or managing utility-scale insights, our API helps you make informed, sustainable choices in real time.

## What you can do with the API

- Access real-time and historical energy consumption data
- Automate alerts for unusual usage patterns
- Sync with third-party smart home platforms
- Customize energy dashboards for homeowners and partners
- Retrieve performance metrics for solar, battery, and grid interactions

## Who it's for

This API is designed for:

- **Developers** building smart energy applications
- **Utilities** needing scalable, real-time grid data
- **Device manufacturers** integrating with GreenGrid hardware
- **Energy consultants** providing personalized efficiency advice

## Getting started

To begin using the GreenGrid API:

1. Sign in to your developer account at [developers.greengrid.io](https://developers.greengrid.io).
2. Create a new project and generate your API keys.
3. Review the authentication guide and rate limits.
4. Explore our interactive documentation and test endpoints directly in your browser.

## Key features

### RESTful structure
Standard HTTP methods (GET, POST, PUT, DELETE) make integration simple and predictable.

### Scalable data access
Our endpoints support millions of requests daily, with secure, low-latency delivery.

### Built-in filtering
Query parameters allow granular access to device-level data, time ranges, and user IDs.

### Error transparency
All responses include clear error codes and remediation guidance to keep your system running smoothly.

## Example endpoints

| Endpoint | Description |
|----------|-------------|
| `GET /devices` | List all registered devices for a user |
| `GET /devices/{id}/usage` | Retrieve energy usage for a specific device |
| `POST /alerts` | Set a new usage or outage alert |
| `GET /analytics/monthly` | Pull month-over-month usage summaries |

## Support and feedback

If you run into issues or have feature suggestions, visit our [Help Center](https://support.greengrid.io) or reach out through our developer forum. We’re here to help you build a greener, smarter energy future.

## Next steps

Explore the [Authentication Guide](https://developers.greengrid.io/auth) or jump straight into the [API Reference](https://developers.greengrid.io/docs).

Ready to power up your integration? Let’s get started.

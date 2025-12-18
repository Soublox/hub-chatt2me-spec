---
title: Getting Started
excerpt: >-
  Thank you for choosing the Hub Chatt2.me. With an Application API Key you can
  send messages through our providers like Instagram and Messenger and manage
  webhooks for your applications.
deprecated: false
hidden: false
icon: 📓
metadata:
  robots: index
---
## What you can do?

* Send Messenger messages
* Send Instagram messages
* Create, list, update, delete webhooks
* View and retry webhook logs

## Environments

* Production base URL: [https://api.chatt2.me](https://api.chatt2.me)
* Use Content-Type: application/json on all requests.

## Get your api key

1. Create your account.
2. Enable multifactor authentication.
3. Create an application.
4. Copy the API key shown on the application screen.
5. Regenerate the key anytime from the Applications tab inside the application screen.

## Authentication

* Send the header: x-api-key: YOUR_APPLICATION_KEY
* Keep keys server-side; do not embed in client apps.

## First-call checklist

* You have an application/channel ID (from).
* You know the recipient ID (to).
* You’re using [https://api.chatt2.me](https://api.chatt2.me) with HTTPS.
* Headers include Content-Type: application/json and x-api-key.
* Payload matches the OpenAPI schema.

## Typical errors

* 400: Invalid payload.
* 401: Invalid API key.
* 404: Application/channel does not match the API key.

## Rate limits

Respect published limits; on 429, back off and retry later.

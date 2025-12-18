---
title: Send an Instagram message
excerpt: >-
  Sends an Instagram Direct message through Meta’s messaging APIs using your
  application’s channel and x-api-key. Supports text and a single attachment
  payload. Returns message identifiers and type for tracking.
api:
  file: openapi-application-api-key.yaml
  operationId: sendInstagramMessage
hidden: false
---
After send you will receive something like that in your webhook:

```json Text
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:08:40.195Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "message":{
            "text":"Hello from chatt2me!"
        }
    }
}
```
```json Image
```

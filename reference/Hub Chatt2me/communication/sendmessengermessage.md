---
title: Send a Facebook Messenger message
excerpt: >-
  Sends a Facebook Messenger message through Meta’s messaging APIs using your
  application’s channel and x-api-key. Supports text plus Messenger-specific
  attachments or quick replies. Returns message identifiers and type for
  tracking.
api:
  file: openapi-application-api-key.yaml
  operationId: sendMessengerMessage
hidden: false
---
After send you will receive something like that in your webhook:

```json
{
    "eventType":"Message",
    "timestamp":"2025-12-18T18:51:43.502Z",
    "channel":"MESSENGER",
    "payload":{
        "recipient":{
            "id":"26203292189261166"
        },
        "messaging_type":"RESPONSE",
        "message":{
            "text":"Hello from chatt2me!"
        }
    }
}
```

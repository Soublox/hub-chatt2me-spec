---
title: Send a message with Facebook Messenger
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
    "eventType":"message_echoes",
    "timestamp":"2025-12-18T19:07:49.977Z",
    "payload":{
        "sender":{
            "id":"847421668462669",
            "pageId":"847421668462669"
        },
        "recipient":{
            "id":"26203292189261166"
        },
        "timestamp":1766084871694,
        "message":{
            "mid":"m_jcSSLLlfIWmAC1MxwvU7n6IC1qiFOEeW3Kd3rVdZw2ZyKXmT23sTmtZ-3ET2uOJijjH33Iqrgz0sS1x63jMppg",
            "is_echo":true,
            "text":"Hello from chatt2me!",
            "app_id":854313003749170
        }
    }
}
```

<br />

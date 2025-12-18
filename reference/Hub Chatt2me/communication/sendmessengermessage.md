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

```json Text
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
```json Image
{
    "eventType":"message_echoes",
    "timestamp":"2025-12-18T19:14:01.824Z",
    "payload":{
        "sender":{
            "id":"847421668462669",
            "pageId":"847421668462669"
        },
        "recipient":{
            "id":"26203292189261166"
        },
        "timestamp":1766085243300,
        "message":{
            "mid":"m_LYLzZftS2ibW-AAEettmeaIC1qiFOEeW3Kd3rVdZw2ZI8eq8ONmT-8hxqvys83zO7kxD4b8ZIz12LFdluB5X-g",
            "is_echo":true,
            "app_id":854313003749170,
            "attachments":[
                {
                    "type":"image",
                    "payload":{
                        "url":"https://scontent-sea5-1.xx.fbcdn.net/v/t1.15752-9/531585713_779941841279814_5933370788157455945_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=eb2e90&_nc_ohc=zgSQBLi0pugQ7kNvwEh1LAk&_nc_oc=AdmznYaYoTQ7MqBkWb9FmuFPIbGTMAYQOV7OXf-n4LtNgxuS7EguAyxT9qCC_3kBhUJVHCppCJGIhxfBbBwomQwu&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent-sea5-1.xx&oh=03_Q7cD4AFQRj7CC22AHDwFkPJKWeq2V8XBBHxZPnQNl0Vmok6qiw&oe=696BB0E1"
                    }
                }
            ]
        }
    }
}
```

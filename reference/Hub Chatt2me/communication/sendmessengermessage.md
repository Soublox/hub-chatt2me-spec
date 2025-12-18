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
```json Audio
{
    "eventType":"message_echoes",
    "timestamp":"2025-12-18T19:16:35.197Z",
    "payload":{
        "sender":{
            "id":"847421668462669",
            "pageId":"847421668462669"
        },
        "recipient":{
            "id":"26203292189261166"
        },
        "timestamp":1766085396386,
        "message":{
            "mid":"m_16rlrSqf_SZcZensx2y5saIC1qiFOEeW3Kd3rVdZw2bDjvVFRQvZ69XcKShKC70B-VuQUGZfYvXfo5ClpR4ndw",
            "is_echo":true,
            "app_id":854313003749170,
            "attachments":[
                {
                    "type":"audio",
                    "payload":{
                        "url":"https://scontent-sea5-1.cdn.fbsbx.com/v/t59.3654-21/594398540_1336743217779384_7274673520964647568_n.mp4/audioclip-1766085393000-8824.mp4?_nc_cat=111&ccb=1-7&_nc_sid=d61c36&_nc_ohc=HMNcclmv9AkQ7kNvwHM9qrB&_nc_oc=AdmgsbK0Lz3YMhJp4a3yvJvtNqUWKaD9YbtxGIL6egjHlku-YHbW7KEmkpVlJtJbhdLqDCYQDJZgMhU4wcKBQ5Mq&_nc_zt=28&_nc_ht=scontent-sea5-1.cdn.fbsbx.com&_nc_gid=86Xk-t1UEcjvymF3rBk9Iw&oh=03_Q7cD4AGaW7fXspEIWZ-teLESQDerdkG5gvxZEDIZwG8rTi6Ckw&oe=694633FA"
                    }
                }
            ]
        }
    }
}
```
```json Video
{
    "eventType":"message_echoes",
    "timestamp":"2025-12-18T19:17:50.400Z",
    "payload":{
        "sender":{
            "id":"847421668462669",
            "pageId":"847421668462669"
        },
        "recipient":{
            "id":"26203292189261166"
        },
        "timestamp":1766085471807,
        "message":{
            "mid":"m_20BC3oeZnZcalu_1E2tm5qIC1qiFOEeW3Kd3rVdZw2YBDe9RKygKOiEURj0mULBpgia7RK9aZaOFw7VOFLb_2g",
            "is_echo":true,
            "app_id":854313003749170,
            "attachments":[
                {
                    "type":"video",
                    "payload":{
                        "url":"https://video-sea1-1.xx.fbcdn.net/v/t42.3356-2/593677095_25785160294423301_922898644984382577_n.mp4?_nc_cat=101&ccb=1-7&_nc_sid=4f86bc&_nc_ohc=Z_-VYjvUPAQQ7kNvwG2A873&_nc_oc=AdkE_3UeG8VnRW48f72rcqHt0CImkHk8N61WVn2vrLmdT_5IL1kzYz7GvBUogWTMxj0f9FL4YSt2VhH57DcjAR_Y&_nc_zt=28&_nc_ht=video-sea1-1.xx&_nc_gid=bvFwAhbPnQsiCgJnDj0H_Q&oh=03_Q7cD4AF7QfTCyG6pAf7pRDvcW9epLJP2y3TgjI3GX6A4RVx-7Q&oe=69462ED1"
                    }
                }
            ]
        }
    }
}
```
```json QuickReply
{
    "eventType":"message_echoes",
    "timestamp":"2025-12-18T19:19:01.034Z",
    "payload":{
        "sender":{
            "id":"847421668462669",
            "pageId":"847421668462669"
        },
        "recipient":{
            "id":"26203292189261166"
        },
        "timestamp":1766085542708,
        "message":{
            "mid":"m_IREPZNkSy5nYfVTdiJ-oyqIC1qiFOEeW3Kd3rVdZw2bWk9RV1fqUPAqnXZ7vimpl0H1BelLlydDViwQjt22M1w",
            "is_echo":true,
            "text":"Como posso ajudar?",
            "app_id":854313003749170
        }
    }
}
```
```json Button
{
    "eventType":"message_echoes",
    "timestamp":"2025-12-18T19:20:12.461Z",
    "payload":{
        "sender":{
            "id":"847421668462669",
            "pageId":"847421668462669"
        },
        "recipient":{
            "id":"26203292189261166"
        },
        "timestamp":1766085614186,
        "message":{
            "mid":"m_ielRXxOyqEZj5HOKF5ozIqIC1qiFOEeW3Kd3rVdZw2ah_eDGCLRbBKkQQ-QigHH7AyltGo5PUrJiek1_AWPexQ",
            "is_echo":true,
            "text":"Tap a button",
            "app_id":854313003749170,
            "attachments":[
                {
                    "type":"template",
                    "title":"Tap a button",
                    "payload":{
                        "template_type":"button",
                        "buttons":[
                            {
                                "type":"web_url",
                                "title":"Abrir",
                                "url":"https://www.messenger.com/"
                            },
                            {
                                "type":"postback",
                                "title":"Falar com suporte",
                                "payload":"SUPORTE"
                            }
                        ]
                    }
                }
            ]
        }
    }
}
```
```json Generic Template
{
    "eventType":"message_echoes",
    "timestamp":"2025-12-18T19:20:16.499Z",
    "payload":{
        "sender":{
            "id":"847421668462669",
            "pageId":"847421668462669"
        },
        "recipient":{
            "id":"26203292189261166"
        },
        "timestamp":1766085618240,
        "message":{
            "mid":"m_WVU2S8KLGtqk-hzsjf0yUaIC1qiFOEeW3Kd3rVdZw2ZkOowbql_QfCJlerTCPkMo8NG6YS4HyMTfarpgmD37xQ",
            "is_echo":true,
            "app_id":854313003749170,
            "attachments":[
                {
                    "type":"template",
                    "title":"Card 1",
                    "payload":{
                        "template_type":"generic",
                        "sharable":false,
                        "elements":[
                            {
                                "title":"Card 1",
                                "image_url":"https://img.odcdn.com.br/wp-content/uploads/2025/03/pokemon-tipo-1920x1080.jpg",
                                "default_action":{
                                    "type":"web_url",
                                    "url":"https://example.com/"
                                },
                                "buttons":[
                                    {
                                        "type":"postback",
                                        "title":"Select",
                                        "payload":"CARD1"
                                    }
                                ],
                                "subtitle":"Subtitle 1"
                            },
                            {
                                "title":"Card 2",
                                "image_url":"https://img.odcdn.com.br/wp-content/uploads/2025/03/pokemon-tipo-1920x1080.jpg",
                                "subtitle":"Subtitle 2"
                            }
                        ]
                    }
                }
            ]
        }
    }
}
```
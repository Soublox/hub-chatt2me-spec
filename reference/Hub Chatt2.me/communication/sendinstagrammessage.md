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
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:20:46.565Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "message":{
            "attachment":{
                "type":"image",
                "payload":{
                    "url":"https://img.odcdn.com.br/wp-content/uploads/2025/03/pokemon-tipo-1920x1080.jpg"
                }
            }
        }
    }
}
```
```json Audio
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:20:53.673Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "message":{
            "attachment":{
                "type":"audio",
                "payload":{
                    "url":"https://lookaside.fbsbx.com/ig_messaging_cdn/?asset_id=1336743214446051&signature=AYePXGxExbZI9-zaEeAHeM8pADWNOfOGDVDGF3IBoyzkk2P5vSP4313mCkvOVHasLIAfCkTyesI6AZHRr4YCjuiGcCVuo6aKQkDUXd5stIJBM17IKa0YVm1CvD-zI_Cqslk6_xTclMUIoGAtnUSSi7MAsqbGfCSsl1VCTWyR3hUjiHYvCNa09PPEajDFUok9p9ReVSDEQFFzSbOFbMGbwwihHta8jNU"
                }
            }
        }
    }
}
```
```json Video
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:21:04.313Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "message":{
            "attachment":{
                "type":"video",
                "payload":{
                    "url":"https://lookaside.fbsbx.com/ig_messaging_cdn/?asset_id=1154048980043118&signature=AYdxC0OFuVRg1k3-1P2U7-zus7__DZEJUFPuRik60A4VH5gk7s4zzFrTeCW364diqG5fYhbxcu1lEx2-oidxa1_o7aH2H9EW9DLj1SvshJiXzdvedcv30znZPoS4N2hxssHwm2jUqbclpowleNfUFgz-j5Ttktm-37ESJhJhyPbJ9o8ErNpURmOVV0nq3kxtQnC83q5gjVmb_4MonO5yc5KO5PxJAwQ"
                }
            }
        }
    }
}
```
```json Sticker
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:21:09.535Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "message":{
            "attachment":{
                "type":"like_heart"
            }
        }
    }
}
```
```json Quick Reply
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:21:14.905Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "message":{
            "text":"Como posso ajudar?",
            "quick_replies":[
                {
                    "content_type":"text",
                    "title":"Suporte",
                    "payload":"SUPORTE"
                },
                {
                    "content_type":"text",
                    "title":"Vendas",
                    "payload":"VENDAS"
                }
            ]
        }
    }
}
```
```json Generic Template
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:21:21.093Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "message":{
            "attachment":{
                "type":"template",
                "payload":{
                    "template_type":"button",
                    "text":"Tap a button",
                    "buttons":[
                        {
                            "type":"web_url",
                            "url":"https://www.messenger.com",
                            "title":"Abrir"
                        },
                        {
                            "type":"postback",
                            "title":"Falar com suporte",
                            "payload":"SUPORTE"
                        }
                    ]
                }
            }
        }
    }
}
```
```json React
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:52:51.178Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "sender_action":"react",
        "payload":{
            "message_id":"aWdfZAG1faXRlbToxOklHTWVzc2FnZAUlEOjE3ODQxNDc4NTIwMzA3MzQyOjM0MDI4MjM2Njg0MTcxMDMwMTI0NDI3NjAzNTI3NzI5ODYzMDkzODozMjU2NTQ3Njc1OTE5NzUwNTY4MjQwMjMzNzY4NDk3OTcxMgZDZD",
            "reaction":"love"
        }
    }
}
```
```json Unreact
{
    "eventType":"Message",
    "timestamp":"2025-12-18T20:52:53.486Z",
    "payload":{
        "recipient":{
            "id":"847495124317323"
        },
        "sender_action":"unreact",
        "payload":{
            "message_id":"aWdfZAG1faXRlbToxOklHTWVzc2FnZAUlEOjE3ODQxNDc4NTIwMzA3MzQyOjM0MDI4MjM2Njg0MTcxMDMwMTI0NDI3NjAzNTI3NzI5ODYzMDkzODozMjU2NTQ3Njc1OTE5NzUwNTY4MjQwMjMzNzY4NDk3OTcxMgZDZD"
        }
    }
}
```
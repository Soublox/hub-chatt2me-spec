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
```
```

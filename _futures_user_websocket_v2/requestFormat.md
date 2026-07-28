---
title: Request message format
position_number: 2
type:
description:
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
        subscribe:
        ```js
          {
             "method": "SUBSCRIBE/UNSUBSCRIBE",
             "params": [
                 "order",
                 "trade",
                 "balance",
                 "position",
                 "notify",
                 "entrust",
                 "profit",
                 "track_entrust",
                 "user_profile",
                 "plan_reverse_entrust"
              ],
             "id": "{id}"    //user defined
          }
        ```

        Channel names are plain (no `@listenKey` suffix). The token is carried at handshake time (see General WSS information); it is not part of the subscribe params.
left_code_blocks:
    -
        code_block:
        title: subscribe
        language: javascript
    -
        code_block:
        title: unsubscribe
        language: javascript
right_code_blocks:
    -
        code_block: |-
               {"method":"SUBSCRIBE",
                "params":["order","position"],
                "id":"test1"
                }
        title: subscribe
        language: json
---

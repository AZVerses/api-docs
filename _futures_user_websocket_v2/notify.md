---
title: Message
position_number: 11
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
           "notify"
        ],
       "id": "{id}"
    }
  ```

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "notify",
                    "data": {
                           "symbol":"btc_usdt",
                           "positionType": "ISOLATED",
                           "positionSide": "LONG",
                           "positionSize":"0.5",  // Position quantity (base coin)
                           "notifyType": "WARN"   // Notification type:WARN:about to be liquidated;PARTIAL:partial liquidation;LIQUIDATION:liquidation;ADL:ADL
                    },
                    "ts": 1731231231000
                }
        title: Response
        language: json
---

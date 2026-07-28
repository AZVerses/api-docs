---
title: 用户消息
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
                           "positionSize":"0.5",  // 持仓数量（标的币）
                           "notifyType": "WARN"   // 通知类型:WARN:告警，即将被强平;PARTIAL:部分强平;LIQUIDATION:全部强平;ADL:自动减仓
                    },
                    "ts": 1731231231000
                }
        title: Response
        language: json
---

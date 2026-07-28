---
title: 追踪委托
position_number: 14
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
           "track_entrust"
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
                "ch": "track_entrust",
                "data": {
                        "trackId": "556931318219666113",     // 追踪委托id
                        "symbol": "btc_usdt",                // 交易对
                        "orderSide": "BUY",                  // 买卖方向 BUY, SELL
                        "positionSide": "LONG",              // LONG, SHORT
                        "configActivation": true,            // 是否配置了激活价
                        "activationPrice": "108000.0",       // 激活价
                        "currentPrice": "107800.0",          // 当前价
                        "origQty": "0.5",                    // 下单数量（标的币）
                        "stopPrice": "107000.0",             // 触发价
                        "triggerPriceType": "LATEST_PRICE",  // 触发价格类型
                        "callback": "RATE",                  // 回调类型
                        "callbackVal": "0.01",               // 回调值
                        "state": "NOT_TRIGGERED",            // 状态
                        "desc": "",                          // 描述
                        "createdTime": 1731231231000,        // 创建时间(ms)
                        "updatedTime": 1731231231000         // 更新时间(ms)
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

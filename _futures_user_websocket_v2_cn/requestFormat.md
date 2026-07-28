---
title: 请求报文格式
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
           "id": "{id}"    //用户自己定义
           }
        ```

        频道名为纯名称（无 `@listenKey` 后缀）。token 在握手阶段携带（见基本信息），不作为订阅参数。
left_code_blocks:
    -
        code_block: 
        title: 订阅
        language: javascript
    -
        code_block: |-
                {
                    "method": "unsubscribe", 
                    "params": [
                        "order"
                    ], 
                    "id": "{id}"   //回调ID
                }
        title: 取消订阅
        language: javascript
right_code_blocks:
    -
        code_block: |-
               {"method":"SUBSCRIBE",
                "params":["order","position"],
                "id":"test1"
               }
        title: Response
        language: json
---

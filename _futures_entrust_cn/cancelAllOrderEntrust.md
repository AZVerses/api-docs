---
title: 撤销所有委托（限价/市价/计划）
position_number: 28
type: post
description: /az/future/trade/v1/order-entrust/cancel-all
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: 交易对，例如btc_usdt（不传时撤销所有交易对委托）
        ranges:
content_markdown: |-

                 #### **限流规则**

                 200/s/apikey
left_code_blocks:
    -
        code_block: 
        title: Java
        language: java
right_code_blocks:
    - code_block: |-
        {
          "error": {
            "code": "",
            "msg": ""
          },
          "msgInfo": "",
          "result": true,
          "returnCode": 0
        }
      title: Response
      language: json
---
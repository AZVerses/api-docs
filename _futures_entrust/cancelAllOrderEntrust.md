---
title: Cancel All Orders and Trigger Orders
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
        description: Trading pair, e.g. btc_usdt (cancels all trading pairs if not passed)
        ranges:
content_markdown: |-

                 #### **Limit Flow Rules**

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
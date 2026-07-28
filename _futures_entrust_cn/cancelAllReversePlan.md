---
title: 撤销所有计划反手
position_number: 23
type: post
description: /az/future/trade/v1/entrust/cancel-all-reverse-plan
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: 交易对，例如btc_usdt（不传时撤销所有交易对）
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
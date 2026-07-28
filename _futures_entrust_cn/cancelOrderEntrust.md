---
title: 撤销委托（限价/市价/计划）
position_number: 27
type: post
description: /az/future/trade/v1/order-entrust/cancel
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: type
        type: string
        mandatory: true
        default: N/A
        description: 类型：ORDER(限价和市价委托);ENTRUST(计划委托)
        ranges: ORDER;ENTRUST
    -
        name: id
        type: integer
        mandatory: true
        default: N/A
        description: id
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
          "result": {},
          "returnCode": 0
        }
      title: Response
      language: json
---
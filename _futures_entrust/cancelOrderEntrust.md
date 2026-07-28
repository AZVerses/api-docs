---
title: Cancel Order or Trigger Order
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
        description: Type:ORDER(limit and market order);ENTRUST(trigger order)
        ranges: ORDER;ENTRUST
    -
        name: id
        type: integer
        mandatory: true
        default: N/A
        description: id
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
          "result": {},
          "returnCode": 0
        }
      title: Response
      language: json
---
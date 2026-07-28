---
title: Cancel Reverse Trigger Orders
position_number: 21
type: post
description: /az/future/trade/v1/entrust/cancel-reverse-plan
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: entrustId
        type: integer
        mandatory: true
        default: N/A
        description: Reverse trigger order ID
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
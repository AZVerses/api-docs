---
title: Alter Reverse Trigger Orders
position_number: 22
type: post
description: /az/future/trade/v1/entrust/update-reverse-plan
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: entrustId
        type: integer
        mandatory: true
        default: N/A
        description: Reverse trigger order ID
        ranges:
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default: N/A
        description: Trigger price type:INDEX_PRICE(Index price)；MARK_PRICE(Mark price)；LATEST_PRICE(latest price)
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: stopPrice
        type: number
        mandatory: true
        default: N/A
        description: Trigger price
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
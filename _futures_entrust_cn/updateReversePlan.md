---
title: 修改计划反手
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
        description: 计划反手id
        ranges:
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default: N/A
        description: 触发价格类型：INDEX_PRICE(指数价格)；MARK_PRICE(标记价格)；LATEST_PRICE(最新价格)
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: stopPrice
        type: number
        mandatory: true
        default: N/A
        description: 触发价格
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
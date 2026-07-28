---
title: Change Position Type
position_number: 17
type: post
description: /az/future/user/v1/position/change-type
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
    -
        name: positionSide
        type: string
        mandatory: false
        default: N/A
        description: Position side
        ranges: LONG;SHORT
    -
        name: positionType
        type: string
        mandatory: true
        default: N/A
        description: Position type
        ranges: CROSSED;ISOLATED
    -
        name: positionTypeAllSymbol
        type: boolean
        mandatory: false
        default: N/A
        description: Whether to apply the position type change to all trading pairs
        ranges:
    -
        name: marginCoin
        type: string
        mandatory: false
        default: quoteCoin
        description: Margin coin (optional, defaults to the quote coin)
        ranges:
content_markdown: |-

              #### **Limit Flow Rules**

              200/s/apikey
left_code_blocks:
    -
        code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/user/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
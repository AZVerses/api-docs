---
title: Cancel All Stop Limit
position_number: 9
type: post
description: /az/future/trade/v1/entrust/cancel-all-profit-stop
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: Trading pair, e.g. btc_usdt (cancels all trading pairs if not passed)
        ranges:
    -
        name: positionType
        type: string
        mandatory: false
        default: N/A
        description: Position type (cancels all position types if not passed)
        ranges: CROSSED;ISOLATED
    -
        name: positionSide
        type: string
        mandatory: false
        default: N/A
        description: Position side (cancels all sides if not passed)
        ranges: LONG;SHORT
    -
        name: closeType
        type: string
        mandatory: false
        default: N/A
        description: Close type (cancels all types if not passed)
        ranges: FIXED;ALL
content_markdown: |-

                 #### **Limit Flow Rules**

                 200/s/apikey
left_code_blocks:
    -
        code_block: "public void getKLine() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getKLine?market=btc_usdt&type=1min&since=0\");\r\n\tSystem.out.println(text);\r\n}"
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
---
title: 撤销所有止盈止损
position_number: 9
type: post
description: /az/future/trade/v1/entrust/cancel-all-profit-stop
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: 
        description: 交易对，例如btc_usdt（不传时撤销所有交易对）
        ranges:
    -
        name: positionType
        type: string
        mandatory: false
        default: N/A
        description: 仓位类型（不传时撤销所有仓位类型）
        ranges: CROSSED;ISOLATED
    -
        name: positionSide
        type: string
        mandatory: false
        default: N/A
        description: 仓位方向（不传时撤销所有方向）
        ranges: LONG;SHORT
    -
        name: closeType
        type: string
        mandatory: false
        default: N/A
        description: 止盈止损平仓类型（不传时撤销所有类型）
        ranges: FIXED;ALL
content_markdown: |-
                 #### **限流规则**

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
---
title: 查询近期成交列表
position_number: 6
type: get
description: /az/spot/public/trade/recent
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '200'
        description: 数量
        ranges: 1，1000
content_markdown: >-
    #### **限流规则**

    10/s/ip

left_code_blocks:
    -
        code_block: |-
            public String tradeRecent(){


            }
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": [
                    {
                      "i": 0,           //ID
                      "t": 0,           //成交时间(time)
                      "s": "btc_usdt",  //交易对(symbol)
                      "p": "string",    //成交价(price)
                      "a": "string",    //成交量(quantity, base)
                      "v": "string",    //成交额(volume, quote)
                      "m": "BID"        //taker方向: BID或ASK
                    }
                  ]
                }
        title: Response
        language: json
---

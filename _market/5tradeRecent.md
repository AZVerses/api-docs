---
title: Query the list of recent transactions
position_number: 6
type: get
description: /az/spot/public/trade/recent
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: trading pair
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '200'
        description: 
        ranges: 1，1000
content_markdown: >-
    #### **Limit Flow Rules**
    
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
                      "t": 0,           //transaction time
                      "s": "btc_usdt",  //symbol
                      "p": "string",    //transaction price
                      "a": "string",    //transaction quantity (base)
                      "v": "string",    //transaction volume (quote)
                      "m": "BID"        //taker side: BID or ASK
                    }
                  ]
                }
        title: Response
        language: json
---

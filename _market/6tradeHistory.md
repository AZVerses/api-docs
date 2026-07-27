---
title: Query historical transaction list
position_number: 7
split: -------------------------------------
type: get
description: /az/spot/public/trade/history
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
    -
        name: direction
        type: string
        mandatory: true
        default:
        description: 'query direction'
        ranges: 'PREV-previous page,NEXT-next page'
    -
        name: fromId
        type: number
        mandatory: false
        default:
        description: 'Start ID，eg: 6216559590087220004'
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**
    
    10/s/ip

left_code_blocks:
    -
        code_block: |-
            public String tradeHistory(){


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
                  "result": {
                    "hasPrev": false,     //has previous page
                    "hasNext": true,      //has next page
                    "items": [
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
                }
        title: Response
        language: json
---

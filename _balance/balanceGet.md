---
title: Get a single currency asset
position_number: 2
type: get
description: /az/spot/balance
parameters:
    -
        name: currency
        type: string
        mandatory: true
        default:
        description: eg:usdt
        ranges:
content_markdown:
left_code_blocks:
    -
        code_block:
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
                    "currency": "usdt",
                    "currencyId": 0,
                    "frozenAmount": "0",       //unavailable (freeze + lock + copy-trade + order + withdraw)
                    "freeze": "0",             //freeze
                    "lock": "0",               //lock
                    "trade": "0",              //order (entrust)
                    "withdraw": "0",           //withdraw
                    "availableAmount": "0",    //available amount
                    "totalAmount": "0",        //total amount
                    "convertBtcAmount": "0",   //converted BTC amount
                    "convertUsdtAmount": "0",  //converted USDT amount
                    "convertAvailableUsdtAmount": "0"  //converted USDT available amount
                  }
                }
        title: Response
        language: json
---


---
title: Get a list of currency assets
position_number: 3
type: get
split: -------------------------------------
description: /az/spot/balances
parameters:
    -
        name: currencies
        type: string
        mandatory: false
        default:
        description: 'List of currencies, comma separated,eg:  usdt,btc'
        ranges:
    -
        name: queryAccountId
        type: long
        mandatory: false
        default:
        description: Query account id. Defaults to the current account id if not passed. A master account is not allowed to be queried
        ranges:
    -
        name: filterIsDisplayFalse
        type: boolean
        mandatory: false
        default: 'true'
        description: Whether to filter out currencies whose isDisplay is false
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**

    10/s/apikey
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
                    "totalUsdtAmount": "0",      //total assets converted to USDT
                    "availableUsdtAmount": "0",  //available assets converted to USDT
                    "totalBtcAmount": "0",       //total assets converted to BTC
                    "assets": [
                      {
                        "currency": "string",
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
                    ]
                  }
                }
        title: Response
        language: json
---


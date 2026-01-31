---
title: Query builder open orders
position_number: 12
type: get
description: /az/spot/builder-order/open-list
parameters:
    -
        name: address
        type: string
        mandatory: false
        default:
        description: user wallet address
        ranges:
    -
        name: fromId
        type: number
        mandatory: false
        default:
        description: start id
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default:
        description: query direction:PREV, NEXT
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '20'
        description: Limit number, max 100
        ranges:
    -
        name: startTime
        type: number
        mandatory: false
        default:
        description: eg:1657682804112
        ranges:
    -
        name: endTime
        type: number
        mandatory: false
        default:
        description: 
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
                "hasPrev": true,
                "hasNext": true,
                "items": [   //For field information, refer to the Get single interface
                  {
                      "address": "0x0804ff769413ffc61e1125af5fbef7bedf26b6eb", //user wallet address
                      "symbol": "mathbb_usdt",
                      "orderId": "587924670845472321",
                      "clientOrderId": "o_2017624598169780225",
                      "baseCurrency": "mathbb",
                      "quoteCurrency": "usdt",
                      "side": "BUY",
                      "type": "LIMIT",
                      "timeInForce": "GTC",
                      "price": "2.0495",
                      "origQty": "0.1095",
                      "origQuoteQty": "0.22442025",
                      "executedQty": "0.0000",
                      "tradeBase": "0.0000",
                      "tradeQuote": "0.0000",
                      "fee": "0",
                      "builderFee": "0",
                      "symbolType": "normal",
                      "closed": false,
                      "state": "NEW",
                      "time": 1769874164641
                  }
                ]
              }
            }
        title: Response
        language: json
---

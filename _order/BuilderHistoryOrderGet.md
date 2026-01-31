---
title: Query builder historical orders
position_number: 11
type: get
description: /az/spot/builder-order/list-history
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
                      "address": "0x0804ff769413ffc61e1125af5fbef7bedf26b6eb",  //User Wallet Address
                      "symbol": "mathbb_usdt",
                      "orderId": "587922216896613953",
                      "clientOrderId": "o_2017622144220921857",
                      "baseCurrency": "mathbb",
                      "quoteCurrency": "usdt",
                      "side": "BUY",
                      "type": "LIMIT",
                      "timeInForce": "GTC",
                      "price": "2.0500",
                      "origQty": "0.1482",
                      "origQuoteQty": "0.30381",
                      "executedQty": "0.1482",
                      "tradeBase": "0.1482",      //Base Currency Executed Quantity
                      "tradeQuote": "0.30120168", //Quote Currency Executed Quantity
                      "avgPrice": "2.0324",
                      "fee": "0.0001",
                      "builderFee": "0",
                      "symbolType": "normal",
                      "closed": true,
                      "state": "FILLED",
                      "time": 1769873579574,
                      "updatedTime": 1769873579620
                  }
                ]
              }
            }
        title: Response
        language: json
---

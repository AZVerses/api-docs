---
title: Query current entrust open orders
position_number: 17
type: get
description: /az/spot/entrust-order/open
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair, if not filled in, represents all
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "SPOT"
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: BUY,SELL
        ranges:
    -
        name: type
        type: string
        mandatory: false
        default:
        description: "entrust order type, only ENTRUST_PROFIT, ENTRUST_TRACK"
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '1000'
        description: Limit number
        ranges: 1，1000
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
                  "result": [      //For field information, refer to the Get single entrust order interface
                    {
                      "id": "6216559590087220004",
                      "clientOrderId": "16559590087220001",
                      "accountId": 123456,
                      "userId": "123456",
                      "symbolId": 1001,
                      "symbol": "BTC_USDT",
                      "side": "1",
                      "type": "3",
                      "timeInForce": "1",
                      "bizType": "1",
                      "price": "40000",
                      "quantity": "2",
                      "quoteQty": "48000",
                      "triggerPrice": "41000",
                      "currentPrice": "40500",
                      "activePrice": "40000",
                      "turnRate": "2",
                      "priceDiff": "2",
                      "extremePrice": "40000",
                      "closed": false,
                      "closedTime": 1655971400834,
                      "state": "1",
                      "activeState": "0",
                      "triggerTime": 0,
                      "triggerState": "0",
                      "rejectReason": "string",
                      "ip": "127.0.0.1",
                      "createdTime": 1655958915583,
                      "updatedTime": 1655958915583
                    }
                  ]
                }
        title: Response
        language: json
---

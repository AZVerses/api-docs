---
title: Query entrust historical orders
position_number: 18
type: get
description: /az/spot/entrust-order/history
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
        name: type
        type: string
        mandatory: false
        default:
        description: "entrust order type, only ENTRUST_PROFIT, ENTRUST_TRACK"
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: BUY,SELL
        ranges:
    -
        name: state
        type: string
        mandatory: false
        default:
        description: 'entrust order state: NEW, TRIGGERED, EXPIRED, CANCELED'
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
    -
        name: hiddenCanceled
        type: bool
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
                "items": [   //For field information, refer to the Get single entrust order interface
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
                    "closed": true,
                    "closedTime": 1655971400834,
                    "state": "2",
                    "activeState": "1",
                    "triggerTime": 1655971400834,
                    "triggerState": "1",
                    "rejectReason": "string",
                    "ip": "127.0.0.1",
                    "createdTime": 1655958915583,
                    "updatedTime": 1655958915583
                  }
                ]
              }
            }
        title: Response
        language: json
---

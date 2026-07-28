---
title: Submit entrust order (TP/SL & tracking)
position_number: 14
type: post
description: /az/spot/entrust-order
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: trading pair
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 'client order id (max 32 chars)'
        ranges:
    -
        name: side
        type: string
        mandatory: true
        default:
        description: "BUY,SELL"
        ranges:
    -
        name: type
        type: string
        mandatory: true
        default:
        description: "entrust order type:ENTRUST_PROFIT(take-profit/stop-loss),ENTRUST_TRACK(tracking order)"
        ranges:
    -
        name: timeInForce
        type: string
        mandatory: true
        default:
        description: effective way:GTC, FOK, IOC, GTX, GTX_SELF_CANCEL
        ranges:
    -
        name: bizType
        type: string
        mandatory: true
        default:
        description: "SPOT"
        ranges:
    -
        name: quantity
        type: number
        mandatory: false
        default:
        description: quantity. Required for TP/SL; required when tracking order sells
        ranges:
    -
        name: quoteQty
        type: number
        mandatory: false
        default:
        description: amount. Not filled for TP/SL; required when tracking order buys
        ranges:
    -
        name: price
        type: number
        mandatory: false
        default:
        description: entrust price, used by TP/SL
        ranges:
    -
        name: triggerPrice
        type: number
        mandatory: false
        default:
        description: trigger price, used by TP/SL
        ranges:
    -
        name: activePrice
        type: number
        mandatory: false
        default:
        description: activation price, used by tracking order (optional)
        ranges:
    -
        name: turnRate
        type: number
        mandatory: false
        default:
        description: callback rate, used by tracking order, between 0.1 and 100
        ranges:
    -
        name: priceDiff
        type: number
        mandatory: false
        default:
        description: price distance, used by tracking order
        ranges:
content_markdown: >-
    #### **Remark**

    ENTRUST_PROFIT is for take-profit/stop-loss orders, triggered by triggerPrice; ENTRUST_TRACK is for tracking orders, driven by activePrice/turnRate/priceDiff.

    #### **Limit Flow Rules**

    20/s/apikey

left_code_blocks:
    -
        code_block: |-
            public String entrustOrderPost(){


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
                  "symbol": "BTC_USDT",
                  "clientOrderId": "16559590087220001",
                  "side": "SELL",
                  "type": "ENTRUST_PROFIT",
                  "timeInForce": "GTC",
                  "bizType": "SPOT",
                  "quantity": 2,
                  "price": 40000,
                  "triggerPrice": 41000
                }
        title: Request
        language: json
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                    "orderId": "6216559590087220004",       // entrust order id
                    "clientOrderId": "16559590087220001"    // client order id
                  }
                }
        title: Response
        language: json
---

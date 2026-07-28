---
title: Create Reverse Trigger Orders
position_number: 20
type: post
description: /az/future/trade/v1/entrust/create-reverse-plan
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: Trading pair
        ranges:
    -
        name: orderSide
        type: string
        mandatory: true
        default: N/A
        description: Order side:BUY;SELL
        ranges: BUY;SELL
    -
        name: origQty
        type: number
        mandatory: true
        default: N/A
        description: Quantity (base coin)
        ranges:
    -
        name: price
        type: number
        mandatory: false
        default: N/A
        description: Price
        ranges:
    -
        name: stopPrice
        type: number
        mandatory: false
        default: N/A
        description: Trigger price
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default: N/A
        description: Position side:LONG;SHORT
        ranges: LONG;SHORT
    -
        name: positionType
        type: string
        mandatory: false
        default: N/A
        description: Position type:CROSSED(Cross margin);ISOLATED(Isolated margin)
        ranges: CROSSED;ISOLATED
    -
        name: timeInForce
        type: string
        mandatory: false
        default: IOC
        description: Valid way:GTC;IOC;FOK;GTX;GTX_SELF_CANCEL
        ranges: GTC;IOC;FOK;GTX;GTX_SELF_CANCEL
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default: N/A
        description: Trigger price type:INDEX_PRICE(Index price)；MARK_PRICE(Mark price)；LATEST_PRICE(latest price)
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: expireTime
        type: integer
        mandatory: false
        default: N/A
        description: Expiration time
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default: N/A
        description: Client order ID
        ranges:
    -
        name: clientMedia
        type: string
        mandatory: false
        default: N/A
        description: Client media
        ranges:
    -
        name: clientMediaChannel
        type: string
        mandatory: false
        default: N/A
        description: Client media channel
        ranges:
content_markdown: |-

                 #### **Limit Flow Rules**

                 200/s/apikey
left_code_blocks:
    -
        code_block: 
        title: Java
        language: java
right_code_blocks:
    - code_block: |-
        {
            "error": {
            "code": "",
            "msg": ""
            },
            "msgInfo": "",
            "result": {},
            "returnCode": 0
        }
      title: Response
      language: json
---
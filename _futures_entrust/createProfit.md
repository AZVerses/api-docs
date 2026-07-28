---
title: Create Stop Limit
position_number: 7
type: post
description: /az/future/trade/v1/entrust/create-profit
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default: N/A
        description: Position side:LONG;SHORT
        ranges: LONG;SHORT
    -
        name: origQty
        type: number
        mandatory: false
        default: N/A
        description: Quantity (base coin)
        ranges:
    -
        name: triggerPriceType
        type: string
        mandatory: false
        default: N/A
        description: Trigger price type:INDEX_PRICE(Index price)；MARK_PRICE(Mark price)；LATEST_PRICE(latest price)
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default: N/A
        description: TP trigger price
        ranges:
    -
        name: triggerStopPrice
        type: number
        mandatory: false
        default: N/A
        description: SL trigger price
        ranges:
    -
        name: closeType
        type: string
        mandatory: false
        default: N/A
        description: Close type:FIXED(Fixed);ALL(All)
        ranges: FIXED;ALL
    -
        name: profitDelegateOrderType
        type: string
        mandatory: false
        default: N/A
        description: TP delegate order type:LIMIT;MARKET
        ranges: LIMIT;MARKET
    -
        name: profitDelegateTimeInForce
        type: string
        mandatory: false
        default: N/A
        description: TP delegate time in force:GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
        ranges: GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
    -
        name: profitDelegatePrice
        type: number
        mandatory: false
        default: N/A
        description: TP delegate price
        ranges:
    -
        name: stopDelegateOrderType
        type: string
        mandatory: false
        default: N/A
        description: SL delegate order type:LIMIT;MARKET
        ranges: LIMIT;MARKET
    -
        name: stopDelegateTimeInForce
        type: string
        mandatory: false
        default: N/A
        description: SL delegate time in force:GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
        ranges: GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
    -
        name: stopDelegatePrice
        type: number
        mandatory: false
        default: N/A
        description: SL delegate price
        ranges:
    -
        name: trackNo
        type: integer
        mandatory: false
        default: N/A
        description: 'trackNo: dedicated order number for copy-trading, pass if the order has one'
        ranges:
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
        code_block: "public void getKLine() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getKLine?market=btc_usdt&type=1min&since=0\");\r\n\tSystem.out.println(text);\r\n}"
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
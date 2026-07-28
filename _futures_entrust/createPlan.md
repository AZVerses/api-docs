---
title: Create Trigger Orders
position_number: 1
type: post
description: /az/future/trade/v1/entrust/create-plan
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default: N/A
        description: Client order ID
        ranges:
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
        name: entrustType
        type: string
        mandatory: true
        default: N/A
        description: >-
            Order type:TAKE_PROFIT(Take Profit Limit Order);STOP(Stop Limit Order);TAKE_PROFIT_MARKET(Take Profit Market Order);STOP_MARKET(Stop Loss Market Order);TRAILING_STOP_MARKET(Trailing Stop Market Order)
        ranges: TAKE_PROFIT;STOP;TAKE_PROFIT_MARKET;STOP_MARKET;TRAILING_STOP_MARKET
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
        name: timeInForce
        type: string
        mandatory: true
        default: N/A
        description: Valid way:GTC;IOC;FOK;GTX;GTX_SELF_CANCEL, Market orders only support IOC
        ranges: GTC;IOC;FOK;GTX;GTX_SELF_CANCEL
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default: N/A
        description: Trigger price type:INDEX_PRICE(Index price)；MARK_PRICE(Mark price)；LATEST_PRICE(latest price)
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
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
        name: marketOrderLevel
        type: integer
        mandatory: false
        default: N/A
        description: 'Best market price level: 1=opponent price; current price; 5,10,15 levels'
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
    -
        name: delegateTriggerPriceType
        type: string
        mandatory: false
        default: N/A
        description: TP/SL trigger price type:INDEX_PRICE(Index price)；MARK_PRICE(Mark price)；LATEST_PRICE(latest price)
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
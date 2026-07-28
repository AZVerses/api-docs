---
title: See Stop Limit
position_number: 10
type: get
description: /az/future/trade/v1/entrust/profit-list
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: "Trading pairs (queries all trading pairs if not passed)\t"
        ranges:
    -
        name: page
        type: integer
        mandatory: false
        default: 1
        description: Page
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: 10
        description: Quantity of a single page
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default: N/A
        description: Start time
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: N/A
        description: End time
        ranges:
    -
        name: state
        type: string
        mandatory: true
        default: N/A
        description: >-
            Order state:NOT_TRIGGERED：New order (not triggered);TRIGGERING:Triggering;TRIGGERED:Triggered;USER_REVOCATION:User revocation;PLATFORM_REVOCATION:Platform revocation (rejection);EXPIRED:expired;UNFINISHED:Unfinished;HISTORY:(History)
        ranges: >-
            NOT_TRIGGERED;TRIGGERING;TRIGGERED;USER_REVOCATION;PLATFORM_REVOCATION;EXPIRED;UNFINISHED;HISTORY
    -
        name: positionType
        type: string
        mandatory: false
        default: N/A
        description: Position type:CROSSED(Cross margin);ISOLATED(Isolated margin)
        ranges: CROSSED;ISOLATED
    -
        name: positionSide
        type: string
        mandatory: false
        default: N/A
        description: Position side:LONG;SHORT
        ranges: LONG;SHORT
    -
        name: closeType
        type: string
        mandatory: false
        default: N/A
        description: TPSL close type:FIXED(Fixed position);ALL(All position)
        ranges: FIXED;ALL
    -
        name: sortType
        type: string
        mandatory: false
        default: N/A
        description: 'TPSL sort type:CTIME(order time);TP_PRICE(SL trigger price);SL_PRICE(TP trigger price)'
        ranges: CTIME;TP_PRICE;SL_PRICE
    -
        name: sortDirection
        type: string
        mandatory: false
        default: N/A
        description: 'TPSL sort direction:ASC(ascending);DESC(descending)'
        ranges: ASC;DESC
content_markdown: |-

                 #### **Limit Flow Rules**

                 200/s/apikey
left_code_blocks:
    -
        code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
          "result": {
            "items": [
              {
                "profitId": 0, //Order ID
                "symbol": "", //Trading pair
                "positionSide": "", //Position side
                "origQty": 0, //Quantity (base coin)
                "leverage": 0, //Leverage
                "triggerPriceType": "", //Trigger price type
                "triggerProfitPrice": 0, //Stop profit price
                "triggerStopPrice": 0, //Stop loss price
                "entryPrice": 0, //Open position average price
                "positionSize": 0, //Position quantity (base coin)
                "isolatedMargin": 0, //Isolated Margin
                "executedQty": 0, //Actual transaction
                "avgPrice": 0, //Actual filled avg price
                "positionType": "", //Position type
                "delegateQty": 0, //Actual delegate quantity
                "delegatePrice": 0, //Actual delegate price
                "profitDelegateOrderType": "", //TP delegate order type
                "profitDelegateTimeInForce": "", //TP delegate time in force
                "profitDelegatePrice": 0, //TP delegate price
                "stopDelegateOrderType": "", //SL delegate order type
                "stopDelegateTimeInForce": "", //SL delegate time in force
                "stopDelegatePrice": 0, //SL delegate price
                "closeType": "", //Close type:FIXED;ALL
                "state": "", //Order state:NOT_TRIGGERED：New order (not triggered);TRIGGERING:Triggering;TRIGGERED:Triggered;USER_REVOCATION:User revocation;PLATFORM_REVOCATION:Platform revocation (rejection);EXPIRED:expired;DELEGATION_FAILED:delegation failed
                "desc": "", //Description (revocation, delegation failure, etc.)
                "triggerPriceSide": "", //Actual trigger side:PROFIT(TP triggered);STOP(SL triggered)
                "createdTime": 0, //Time
                "updatedTime": 0, //Last update time
                "sourceType": "" //Source type
              }
            ],
            "page": 0,
            "ps": 0,
            "total": 0
          },
          "returnCode": 0
        }
      title: Response
      language: json
---
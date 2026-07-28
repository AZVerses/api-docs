---
title: See Reverse Trigger Orders
position_number: 24
type: get
description: /az/future/trade/v1/entrust/reverse-plan-list
parameters:
    -
        name: symbol
        type: string
        mandatory: false
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
          "result": {
            "items": [
              {
                "clientOrderId": "", //Client order ID
                "closePosition": false, //Whether triggered to close all
                "createdTime": 0, //Create time
                "updatedTime": 0, //Update time
                "entrustId": 0, //Order ID
                "entrustType": "", //Order type
                "marketOrderLevel": 0, //Best market price
                "orderSide": "", //Order side
                "ordinary": true,
                "origQty": 0, //Quantity (base coin)
                "positionSide": "", //Position side
                "price": 0, //Order price
                "state": "", //Order state:NOT_TRIGGERED：New order (not triggered);TRIGGERING:Triggering;TRIGGERED:Triggered;USER_REVOCATION:User revocation;PLATFORM_REVOCATION:Platform revocation (rejection);EXPIRED:expired
                "stopPrice": 0, //Trigger price
                "symbol": "", //Trading pair
                "timeInForce": "", //Valid way
                "triggerPriceType": "", //Trigger price type
                "executedQty": 0, //Actual filled quantity (base coin)
                "avgPrice": 0, //Actual filled avg price
                "delegateTriggerPriceType": "", //TP/SL trigger price type
                "triggerProfitPrice": 0, //TP trigger price
                "triggerStopPrice": 0, //SL trigger price
                "profitDelegateOrderType": "", //TP delegate order type
                "profitDelegateTimeInForce": "", //TP delegate time in force
                "profitDelegatePrice": 0, //TP delegate price
                "stopDelegateOrderType": "", //SL delegate order type
                "stopDelegateTimeInForce": "", //SL delegate time in force
                "stopDelegatePrice": 0, //SL delegate price
                "reverseOpenExecutedQty": 0, //Reverse open filled quantity (base coin)
                "reverseOpenAvgPrice": 0, //Reverse open filled avg price
                "reverseOrderId": 0, //Reverse order ID
                "reverseOpenOrderId": 0 //Reverse open order ID
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
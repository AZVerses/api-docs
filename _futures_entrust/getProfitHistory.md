---
title: See Stop Limit History
position_number: 26
type: get
description: /az/future/trade/v1/entrust/profit-list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: "Trading pairs (queries all trading pairs if not passed)\t"
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "Direction（PREV:Previous page；NEXT:Next page）\t"
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default: N/A
        description: id
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: "Limit\t"
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
            "hasNext": false, //Is there a next page
            "hasPrev": false, //Is there a previous page
            "items": [ //Datasheets
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
                "state": "", //Order state:TRIGGERED:Triggered;USER_REVOCATION:User revocation;PLATFORM_REVOCATION:Platform revocation (rejection);EXPIRED:expired;DELEGATION_FAILED:delegation failed
                "desc": "", //Description (revocation, delegation failure, etc.)
                "triggerPriceSide": "", //Actual trigger side:PROFIT(TP triggered);STOP(SL triggered)
                "createdTime": 0, //Time
                "updatedTime": 0, //Last update time
                "sourceType": "" //Source type
              }
            ]
          },
          "returnCode": 0
        }
      title: Response
      language: json
---
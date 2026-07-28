---
title: See Stop Limit base on Profitld
position_number: 11
type: get
description: /az/future/trade/v1/entrust/profit-detail
parameters:
    -
        name: profitId
        type: integer
        mandatory: true
        default: N/A
        description: Stop limit ID
        ranges:
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
          },
          "returnCode": 0
        }
      title: Response
      language: json
---
---
title: See Trigger Orders base on EntrustId
position_number: 5
type: get
description: /az/future/trade/v1/entrust/plan-detail
parameters:
    -
        name: entrustId
        type: integer
        mandatory: true
        default: N/A
        description: Order ID
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
            "closePosition": false, //Whether triggered to close all
            "createdTime": 0, //Create time
            "entrustId": 0, //Order ID
            "entrustType": "", //Order type
            "marketOrderLevel": 0, //Best market price
            "orderSide": "", //Order side
            "ordinary": true,
            "origQty": 0, //Quantity (base coin)
            "positionSide": "", //Position side
            "price": 0, //Order price
            "state": "", //Order state:NOT_TRIGGERED：New order (not triggered);TRIGGERING:Triggering;TRIGGERED:Triggered;USER_REVOCATION:User revocation;PLATFORM_REVOCATION:Platform revocation (rejection);EXPIRED:expired;UNFINISHED:Unfinished;HISTORY:(History)
            "stopPrice": 0, //Trigger price
            "symbol": "", //Trading pair
            "timeInForce": "", //Valid way
            "triggerPriceType": "", //Trigger price type
            "updatedTime": 0, //Update time
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
          },
          "returnCode": 0
        }
      title: Response
      language: json
---
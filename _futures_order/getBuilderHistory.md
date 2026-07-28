---
title: See Builder Order History
position_number: 10
type: get
description: /az/future/user/v1/builder/order/list-history
parameters:
    -
        name: address
        type: string
        mandatory: true
        default: N/A
        description: "User Wallet Address"
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
  - code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
          "hasNext": false,                     //Is there a next page
          "hasPrev": false,                     //Is there a previous page
          "items": [ 
            {
                "orderId": "588227439032729152",          //Order ID
                "clientOrderId": "o_2017927366688374785", //client order id
                "symbol": "mathbb_usdt",                  //Trading pair
                "orderSide": "SELL",                      //Order side
                "orderType": "LIMIT",                     //Order type
                "price": "2.0283",                        //Order price
                "origQty": "494",                         //Quantity (base)
                "avgPrice": "2.0284",
                "executedQty": "494",                     //Volume (base)
                "marginFrozen": "0",                      //Occupied margin
                "state": "FILLED",                        //Order state:NEW：New order (unfilled);PARTIALLY_FILLED:Partial deal;PARTIALLY_CANCELED:Partial revocation;FILLED:Filled;CANCELED:Cancled;REJECTED:Order failed;EXPIRED：Expired
                "positionSide": "SHORT",                  //Position side
                "positionType": "CROSSED",                //Position type
                "timeInForce": "GTC",                     //Valid type
                "closePosition": false,                   //Whether to close all when order condition is triggered
                "forceClose": false,                      //Is it a liquidation order
                "leverage": 1,
                "fee": "0.00230466",                      //Fee
                "builderFee": "0.0006914",                //Builder fee
                "createdTime": 1769946350202,
                "updatedTime": 1769946350254
            }
          ]
        },
        "returnCode": 0
      }
    title: Response
    language: json
---
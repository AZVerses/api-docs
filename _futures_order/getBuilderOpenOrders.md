---
title: See Builder Open Orders
position_number: 11
type: get
description: /az/future/user/v1/builder/order/open-list
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
          "total": 7,
          "size": 7,
          "content": [
            {
                "orderId": "587874928073152192", //Order id
                "symbol": "atom_usdt",           //Trading pair
                "orderSide": "BUY",              //Order side
                "orderType": "LIMIT",            //Order type
                "price": "4.92",                 //Order price
                "contractSize": 1.0,             //Contract size
                "origQty": "1000",               //Quantity (Cont)
                "avgPrice": "4.92",              //Average Price
                "executedQty": "167",            //Volume (Cont)
                "marginFrozen": "412.05",        //Occupied margin
                "state": "PARTIALLY_FILLED",     //Order State NEW,PLACED,PARTIALLY_FILLED
                "positionSide": "LONG",          //Position side
                "positionType": "CROSSED",       //Position type
                "timeInForce": "GTC",            //Valid type
                "closePosition": false,
                "forceClose": false,
                "leverage": 10,
                "fee": "0.082164",
                "builderFee": "0.0246492",
                "createdTime": 1769862305040,
                "updatedTime": 1769865002542
            }
          ]
        },
        "returnCode": 0
      }
    title: Response
    language: json
---
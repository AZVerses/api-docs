---
title: 查询Builder历史订单
position_number: 10
type: get
description: /az/future/user/v1/builder/order/list-history
parameters:
    -
        name: address
        type: string
        mandatory: false
        default: N/A
        description: 用户钱包地址
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "方向（PREV:上一页；NEXT:下一页）\t"
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
        description: "条数\t"
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default: N/A
        description: 起始时间
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: N/A
        description: 结束时间
        ranges:
content_markdown: |-

                  #### **限流规则**

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
          "hasNext": false,                     //是否有下一页
          "hasPrev": false,                     //是否有上一页
          "items": [ 
            {
                "orderId": "588227439032729152",  //订单id
                "clientOrderId": "o_2017927366688374785",
                "symbol": "mathbb_usdt",          //交易对
                "orderSide": "SELL",              //买卖方向
                "orderType": "LIMIT",             //订单类型
                "price": "2.0283",                //委托价格
                "contractSize": 0.01,             //合约面值
                "origQty": "494",                 //数量（张）
                "avgPrice": "2.0284",             //实际成交均价
                "executedQty": "494",             //已成交数量（张）
                "marginFrozen": "0",              //占用保证金
                "state": "FILLED",                //订单状态 NEW：新建订单（未成交）；PARTIALLY_FILLED：部分成交；PARTIALLY_CANCELED：部分撤销；FILLED：全部成交；CANCELED：已撤销；REJECTED：下单失败；EXPIRED：已过期
                "positionSide": "SHORT",          //持仓方向
                "positionType": "CROSSED",        //仓位类型
                "timeInForce": "GTC",             //有效类型
                "closePosition": false,           //是否条件全平仓
                "forceClose": false,              //是否是强平订单
                "leverage": 1,
                "fee": "0.00230466",              //手续费
                "builderFee": "0.0006914",        //builder手续费
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
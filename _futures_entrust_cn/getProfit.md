---
title: 查询止盈止损
position_number: 10
type: get
description: /az/future/trade/v1/entrust/profit-list
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: "交易对（不传时撤销所有交易对）\t"
        ranges:
    -
        name: page
        type: integer
        mandatory: false
        default: 1
        description: 页码
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: 10
        description: 单页数
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default: N/A
        description: 开始时间
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: N/A
        description: 结束时间
        ranges:
    -
        name: state
        type: string
        mandatory: true
        default: N/A
        description: >-
            委托状态
            NOT_TRIGGERED：新建委托（未触发）；TRIGGERING：触发中；TRIGGERED：已触发；USER_REVOCATION：用户撤销；PLATFORM_REVOCATION：平台撤销（拒绝）；EXPIRED：已过期；UNFINISHED：未完成；HISTORY：（历史）
        ranges: >-
            NOT_TRIGGERED;TRIGGERING;TRIGGERED;USER_REVOCATION;PLATFORM_REVOCATION;EXPIRED;UNFINISHED;HISTORY
    -
        name: positionType
        type: string
        mandatory: false
        default: N/A
        description: 仓位模式：CROSSED(全仓);ISOLATED(逐仓)
        ranges: CROSSED;ISOLATED
    -
        name: positionSide
        type: string
        mandatory: false
        default: N/A
        description: 仓位方向：LONG(多仓);SHORT(空仓)
        ranges: LONG;SHORT
    -
        name: closeType
        type: string
        mandatory: false
        default: N/A
        description: TPSL平仓类型：FIXED(固定仓位);ALL(全部仓位)
        ranges: FIXED;ALL
    -
        name: sortType
        type: string
        mandatory: false
        default: N/A
        description: 'TPSL排序方式：CTIME(委托时间);TP_PRICE(止损触发价格);SL_PRICE(止盈触发价格)'
        ranges: CTIME;TP_PRICE;SL_PRICE
    -
        name: sortDirection
        type: string
        mandatory: false
        default: N/A
        description: 'TPSL排序方向：ASC(升序);DESC(降序)'
        ranges: ASC;DESC
content_markdown: |-

               #### **限流规则**

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
                "profitId": 0, //委托id
                "symbol": "", //交易对
                "positionSide": "", //仓位方向
                "origQty": 0, //数量（base 币）
                "leverage": 0, //杠杆倍数
                "triggerPriceType": "", //触发价格类型
                "triggerProfitPrice": 0, //止盈价格
                "triggerStopPrice": 0, //止损价格
                "entryPrice": 0, //开仓均价
                "positionSize": 0, //持仓数量（base 币）
                "isolatedMargin": 0, //逐仓保证金
                "executedQty": 0, //实际成交
                "avgPrice": 0, //实际成交均价
                "positionType": "", //仓位类型
                "delegateQty": 0, //实际委托数量
                "delegatePrice": 0, //实际委托价格
                "profitDelegateOrderType": "", //止盈委托订单类型
                "profitDelegateTimeInForce": "", //止盈委托有效方式
                "profitDelegatePrice": 0, //止盈委托委托价格
                "stopDelegateOrderType": "", //止损委托订单类型
                "stopDelegateTimeInForce": "", //止损委托有效方式
                "stopDelegatePrice": 0, //止损委托价格
                "closeType": "", //平仓类型：FIXED 固定 ALL 全部
                "state": "", //订单状态 NOT_TRIGGERED：新建委托（未触发）；TRIGGERING：触发中；TRIGGERED：已触发；USER_REVOCATION：用户撤销；PLATFORM_REVOCATION：平台撤销（拒绝）；EXPIRED：已过期；DELEGATION_FAILED：委托失败
                "desc": "", //描述，撤销、委托失败等描述
                "triggerPriceSide": "", //实际触发方式：PROFIT 止盈触发,STOP 止损触发
                "createdTime": 0, //时间
                "updatedTime": 0, //最后变更时间
                "sourceType": "" //来源
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
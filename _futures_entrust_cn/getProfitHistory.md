---
title: 查询历史止盈止损
position_number: 26
type: get
description: /az/future/trade/v1/entrust/profit-list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: "交易对（不传时查询所有交易对）\t"
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
            "hasNext": false, //是否有下一页
            "hasPrev": false, //是否有上一页
            "items": [ //数据列表
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
                "state": "", //订单状态 TRIGGERED：已触发；USER_REVOCATION：用户撤销；PLATFORM_REVOCATION：平台撤销（拒绝）；EXPIRED：已过期；DELEGATION_FAILED：委托失败
                "desc": "", //描述，撤销、委托失败等描述
                "triggerPriceSide": "", //实际触发方式：PROFIT 止盈触发,STOP 止损触发
                "createdTime": 0, //时间
                "updatedTime": 0, //最后变更时间
                "sourceType": "" //来源
              }
            ]
          },
          "returnCode": 0
        }
      title: Response
      language: json
---
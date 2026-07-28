---
title: 查询历史计划反手
position_number: 25
type: get
description: /az/future/trade/v1/entrust/reverse-plan-list-history
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
                "clientOrderId": "", //自定义订单id
                "closePosition": false, //是否触发全平
                "createdTime": 0, //创建时间
                "updatedTime": 0, //更新时间
                "entrustId": 0, //委托id
                "entrustType": "", //委托类型
                "marketOrderLevel": 0, //市价最优档
                "orderSide": "", //买卖方向
                "ordinary": true,
                "origQty": 0, //数量（base 币）
                "positionSide": "", //持仓方向
                "price": 0, //订单价格
                "state": "", //订单状态 TRIGGERED：已触发；USER_REVOCATION：用户撤销；PLATFORM_REVOCATION：平台撤销（拒绝）；EXPIRED：已过期
                "stopPrice": 0, //触发价格
                "symbol": "", //交易对
                "timeInForce": "", //有效方式
                "triggerPriceType": "", //触发价格类型
                "executedQty": 0, //实际成交数量（base 币）
                "avgPrice": 0, //实际成交均价
                "delegateTriggerPriceType": "", //止盈止损触发价格类型
                "triggerProfitPrice": 0, //止盈触发价
                "triggerStopPrice": 0, //止损触发价
                "profitDelegateOrderType": "", //止盈委托订单类型
                "profitDelegateTimeInForce": "", //止盈委托有效方式
                "profitDelegatePrice": 0, //止盈委托委托价格
                "stopDelegateOrderType": "", //止损委托订单类型
                "stopDelegateTimeInForce": "", //止损委托有效方式
                "stopDelegatePrice": 0, //止损委托价格
                "reverseOpenExecutedQty": 0, //反手开仓实际成交数量（base 币）
                "reverseOpenAvgPrice": 0, //反手开仓实际成交均价
                "reverseOrderId": 0, //反手订单id
                "reverseOpenOrderId": 0 //反手开仓订单id
              }
            ]
          },
          "returnCode": 0
        }
      title: Response
      language: json
---
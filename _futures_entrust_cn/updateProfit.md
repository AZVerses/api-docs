---
title: 修改止盈止损
position_number: 12
type: post
description: /az/future/trade/v1/entrust/update-profit-stop
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
  - name: profitId
    type: integer
    mandatory: true
    default: N/A
    description: 止盈止损id
    ranges:
  - name: triggerProfitPrice
    type: number
    mandatory: false
    default: N/A
    description: 止盈触发价s
    ranges:
  - name: triggerStopPrice
    type: number
    mandatory: false
    default: N/A
    description: 止损触发价
    ranges:
  - name: triggerPriceType
    type: string
    mandatory: false
    default: N/A
    description: 触发价格类型：INDEX_PRICE(指数价格)；MARK_PRICE(标记价格)；LATEST_PRICE(最新价格)
    ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
  - name: origQty
    type: number
    mandatory: false
    default: N/A
    description: 数量（base 币）
    ranges:
  - name: closeType
    type: string
    mandatory: false
    default: N/A
    description: 平仓类型：FIXED(固定);ALL(全部)
    ranges: FIXED;ALL
  - name: profitDelegateOrderType
    type: string
    mandatory: false
    default: N/A
    description: 止盈委托订单类型：LIMIT(限价);MARKET(市价)
    ranges: LIMIT;MARKET
  - name: profitDelegateTimeInForce
    type: string
    mandatory: false
    default: N/A
    description: 止盈委托有效方式：GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
    ranges: GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
  - name: profitDelegatePrice
    type: number
    mandatory: false
    default: N/A
    description: 止盈委托委托价格
    ranges:
  - name: stopDelegateOrderType
    type: string
    mandatory: false
    default: N/A
    description: 止损委托订单类型：LIMIT(限价);MARKET(市价)
    ranges: LIMIT;MARKET
  - name: stopDelegateTimeInForce
    type: string
    mandatory: false
    default: N/A
    description: 止损委托有效方式：GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
    ranges: GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
  - name: stopDelegatePrice
    type: number
    mandatory: false
    default: N/A
    description: 止损委托价格
    ranges:
content_markdown: |-

               #### **限流规则**

               200/s/apikey
right_code_blocks:
  - code_block: |-
      {
        "error": {
          "code": "",
          "msg": ""
        },
        "msgInfo": "",
        "result": {},
        "returnCode": 0
      }
    title: Response
    language: json
---
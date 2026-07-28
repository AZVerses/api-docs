---
title: 创建计划反手
position_number: 20
type: post
description: /az/future/trade/v1/entrust/create-reverse-plan
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对
        ranges:
    -
        name: orderSide
        type: string
        mandatory: true
        default: N/A
        description: 买卖方向：BUY;SELL
        ranges: BUY;SELL
    -
        name: origQty
        type: number
        mandatory: true
        default: N/A
        description: 数量（base 币）
        ranges:
    -
        name: price
        type: number
        mandatory: false
        default: N/A
        description: 价格
        ranges:
    -
        name: stopPrice
        type: number
        mandatory: false
        default: N/A
        description: 触发价
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default: N/A
        description: 仓位方向：LONG;SHORT
        ranges: LONG;SHORT
    -
        name: positionType
        type: string
        mandatory: false
        default: N/A
        description: 仓位模式：CROSSED(全仓);ISOLATED(逐仓)
        ranges: CROSSED;ISOLATED
    -
        name: timeInForce
        type: string
        mandatory: false
        default: IOC
        description: 有效方式：GTC;IOC;FOK;GTX;GTX_SELF_CANCEL
        ranges: GTC;IOC;FOK;GTX;GTX_SELF_CANCEL
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default: N/A
        description: 触发价格类型：INDEX_PRICE(指数价格)；MARK_PRICE(标记价格)；LATEST_PRICE(最新价格)
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: expireTime
        type: integer
        mandatory: false
        default: N/A
        description: 过期时间
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default: N/A
        description: 客户端ID
        ranges:
    -
        name: clientMedia
        type: string
        mandatory: false
        default: N/A
        description: 客户端媒体
        ranges:
    -
        name: clientMediaChannel
        type: string
        mandatory: false
        default: N/A
        description: 客户端媒体渠道
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
            "result": {},
            "returnCode": 0
        }
      title: Response
      language: json
---
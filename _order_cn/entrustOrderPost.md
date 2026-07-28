---
title: 委托下单（止盈止损/跟踪委托）
position_number: 14
type: post
description: /az/spot/entrust-order
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 客户端ID（最长32位）
        ranges:
    -
        name: side
        type: string
        mandatory: true
        default:
        description: "买卖方向 BUY-买,SELL-卖"
        ranges:
    -
        name: type
        type: string
        mandatory: true
        default:
        description: "委托类型 ENTRUST_PROFIT-止盈止损,ENTRUST_TRACK-跟踪委托"
        ranges:
    -
        name: timeInForce
        type: string
        mandatory: true
        default:
        description: 有效方式 GTC, FOK, IOC, GTX, GTX_SELF_CANCEL
        ranges:
    -
        name: bizType
        type: string
        mandatory: true
        default:
        description: "业务类型 SPOT-现货"
        ranges:
    -
        name: quantity
        type: number
        mandatory: false
        default:
        description: 数量。止盈止损必填；跟踪委托卖出时必填
        ranges:
    -
        name: quoteQty
        type: number
        mandatory: false
        default:
        description: 金额。止盈止损不填；跟踪委托买入时必填
        ranges:
    -
        name: price
        type: number
        mandatory: false
        default:
        description: 委托价格，止盈止损使用
        ranges:
    -
        name: triggerPrice
        type: number
        mandatory: false
        default:
        description: 触发价格，止盈止损使用
        ranges:
    -
        name: activePrice
        type: number
        mandatory: false
        default:
        description: 激活价格，跟踪委托使用（非必填）
        ranges:
    -
        name: turnRate
        type: number
        mandatory: false
        default:
        description: 回调幅度，跟踪委托使用，0.1-100之间
        ranges:
    -
        name: priceDiff
        type: number
        mandatory: false
        default:
        description: 价距，跟踪委托使用
        ranges:
content_markdown: >-
    #### **备注**

    ENTRUST_PROFIT 为止盈止损委托，由 triggerPrice 触发；ENTRUST_TRACK 为跟踪委托，由 activePrice/turnRate/priceDiff 驱动。

    #### **限流规则**

    20/s/apikey

left_code_blocks:
    -
        code_block: |-
            public String entrustOrderPost(){


            }
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                  "symbol": "BTC_USDT",
                  "clientOrderId": "16559590087220001",
                  "side": "SELL",
                  "type": "ENTRUST_PROFIT",
                  "timeInForce": "GTC",
                  "bizType": "SPOT",
                  "quantity": 2,
                  "price": 40000,
                  "triggerPrice": 41000
                }
        title: Request
        language: json
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                    "orderId": "6216559590087220004",       //委托订单ID
                    "clientOrderId": "16559590087220001"    //客户端订单号
                  }
                }
        title: Response
        language: json
---

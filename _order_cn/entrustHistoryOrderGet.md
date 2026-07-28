---
title: 委托历史订单查询
position_number: 18
type: get
description: /az/spot/entrust-order/history
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对，不传代表所有
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "业务类型 SPOT-现货"
        ranges:
    -
        name: type
        type: string
        mandatory: false
        default:
        description: "委托类型，仅限 ENTRUST_PROFIT, ENTRUST_TRACK"
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: BUY-买,SELL-卖
        ranges:
    -
        name: state
        type: string
        mandatory: false
        default:
        description: '委托订单状态：NEW-新建, TRIGGERED-已触发, EXPIRED-已过期, CANCELED-已撤销'
        ranges:
    -
        name: fromId
        type: number
        mandatory: false
        default:
        description: 起始ID
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default:
        description: 查询方向:PREV, NEXT
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '20'
        description: 限制数量,最大100
        ranges:
    -
        name: startTime
        type: number
        mandatory: false
        default:
        description: 开始时间 eg:1657682804112
        ranges:
    -
        name: endTime
        type: number
        mandatory: false
        default:
        description: 结束时间
        ranges:
    -
        name: hiddenCanceled
        type: bool
        mandatory: false
        default:
        description: 隐藏已取消
        ranges:
content_markdown: >-
    #### **限流规则**

    10/s/apikey
left_code_blocks:
    -
        code_block:
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
              "rc": 0,
              "mc": "string",
              "ma": [
                {}
              ],
              "result": {
                "hasPrev": true,
                "hasNext": true,
                "items": [   //字段信息参考委托单笔获取接口
                  {
                    "id": "6216559590087220004",
                    "clientOrderId": "16559590087220001",
                    "accountId": 123456,
                    "userId": "123456",
                    "symbolId": 1001,
                    "symbol": "BTC_USDT",
                    "side": "1",
                    "type": "3",
                    "timeInForce": "1",
                    "bizType": "1",
                    "price": "40000",
                    "quantity": "2",
                    "quoteQty": "48000",
                    "triggerPrice": "41000",
                    "currentPrice": "40500",
                    "activePrice": "40000",
                    "turnRate": "2",
                    "priceDiff": "2",
                    "extremePrice": "40000",
                    "closed": true,
                    "closedTime": 1655971400834,
                    "state": "2",
                    "activeState": "1",
                    "triggerTime": 1655971400834,
                    "triggerState": "1",
                    "rejectReason": "string",
                    "ip": "127.0.0.1",
                    "createdTime": 1655958915583,
                    "updatedTime": 1655958915583
                  }
                ]
              }
            }
        title: Response
        language: json
---

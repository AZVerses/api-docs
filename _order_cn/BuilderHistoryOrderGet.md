---
title: builder历史订单查询
position_number: 11
type: get
description: /az/spot/builder-order/list-history
parameters:
    -
        name: address
        type: string
        mandatory: false
        default:
        description: 用户钱包地址
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
                "items": [   //内容信息参考单笔获取订单接口
                  {
                    "address": "0x0804ff769413ffc61e1125af5fbef7bedf26b6eb",  //用户钱包地址
                    "symbol": "mathbb_usdt",
                    "orderId": "587922216896613953",
                    "clientOrderId": "o_2017622144220921857",
                    "baseCurrency": "mathbb",
                    "quoteCurrency": "usdt",
                    "side": "BUY",
                    "type": "LIMIT",
                    "timeInForce": "GTC",
                    "price": "2.0500",
                    "origQty": "0.1482",
                    "origQuoteQty": "0.30381",
                    "executedQty": "0.1482",
                    "tradeBase": "0.1482",      //成交标的(成交数量)
                    "tradeQuote": "0.30120168", //成交报价(成交金额)
                    "avgPrice": "2.0324",
                    "fee": "0.0001",
                    "builderFee": "0",
                    "symbolType": "normal",
                    "closed": true,
                    "state": "FILLED",
                    "time": 1769873579574,
                    "updatedTime": 1769873579620
                  }
                ]
              }
            }
        title: Response
        language: json
---

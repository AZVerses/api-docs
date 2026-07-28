---
title: 查询当前挂单
position_number: 8
type: get
description: /az/spot/open-order
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
        description: >-
            业务类型  SPOT-现货, PREDICTION-预测市场
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: BUY-买,SELL-卖
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '1000'
        description: 限制数量
        ranges: 1，1000
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
                  "result": [      //字段信息参考单笔订单获取接口
                    {
                      "symbol": "BTC_USDT",
                      "orderId": "6216559590087220004",
                      "clientOrderId": "16559590087220001",
                      "rfq": false,
                      "baseCurrency": "string",
                      "quoteCurrency": "string",
                      "side": "BUY",
                      "type": "LIMIT",
                      "timeInForce": "GTC",
                      "price": "40000",
                      "origQty": "2",
                      "origQuoteQty": "48000",
                      "executedQty": "1.2",
                      "leavingQty": "string",
                      "tradeBase": "2",
                      "tradeQuote": "48000",
                      "avgPrice": "42350",
                      "fee": "string",
                      "feeCurrency": "string",
                      "nftId": "string",
                      "symbolType": "normal",
                      "origRestFee": "string",
                      "origFeeCurrency": "string",
                      "platFormCurrencyFee": "string",
                      "platFormCurrency": "string",
                      "couponAmount": "string",
                      "couponCurrency": "string",
                      "couponDeductFee": "string",
                      "closed": false,
                      "state": "NEW",
                      "time": 1655958915583,
                      "ip": "127.0.0.1",
                      "updatedTime": 1655958915583
                    }
                  ]
                }
        title: Response
        language: json
---

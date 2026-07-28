---
title: Query the current pending order
position_number: 8
type: get
description: /az/spot/open-order
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair, if not filled in, represents all
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "SPOT, PREDICTION"
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: BUY,SELL
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '1000'
        description: Limit number
        ranges: 1，1000
content_markdown: >-
    #### **Limit Flow Rules**

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
                  "result": [      //For field information, refer to the Get single interface
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

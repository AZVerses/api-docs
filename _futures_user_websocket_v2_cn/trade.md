---
title: 用户成交
position_number: 9
type:
description: 

parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
  subscribe:
  ```js
    {
       "method": "SUBSCRIBE/UNSUBSCRIBE",
       "params": [
           "trade"
        ],
       "id": "{id}"
    }
  ```

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "trade",
                "data": {
                        "id": "556931318219666113",
                        "symbol": "btc_usdt",     //交易对
                        "orderSide": "BUY",       //订单方向
                        "positionSide": "LONG",   //持仓方向
                        "orderId":"12312312",     //订单id
                        "price":"34244",          //价格
                        "quantity":"0.5",         //数量（标的币）
                        "isMaker": true,          //是否是maker,true:maker;false:taker
                        "marginUnfrozen":"123",   //保证金解冻数量
                        "fee": "0.0002",          //手续费（字符串）
                        "timestamp":1731231231000, //时间戳(ms)
                        "clientOrderId":"123456", //自定义订单id
                        "oppositeUserId": "1234", //对手方用户id，仅提供给做市商/Vault账户
                        "oppositeOrderId": "2345",//对手方订单id，仅提供给做市商/Vault账户
                        "execId": "123",          //成交id，仅提供给做市商/Vault账户
                        "searchId": "789"         //检索id，仅提供给做市商/Vault账户
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

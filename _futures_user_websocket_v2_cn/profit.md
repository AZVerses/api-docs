---
title: 止盈止损
position_number: 13
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
           "profit"
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
                "ch": "profit",
                "data": {
                        "accountId": 8654006125462,
                        "accountType": 0,
                        "profitId": "556931318219666113",       // 止盈止损id
                        "symbol": "btc_usdt",                   // 交易对
                        "positionSide": "LONG",                 // LONG, SHORT
                        "origQty": "0.5",                       // 数量（标的币）
                        "triggerPriceType": "LATEST_PRICE",     // 触发价格类型
                        "triggerProfitPrice": "120000.0",       // 止盈触发价
                        "triggerStopPrice": "100000.0",         // 止损触发价
                        "profitDelegateOrderType": "MARKET",    // 止盈委托订单类型
                        "profitDelegateTimeInForce": "GTC",     // 止盈委托有效方式
                        "profitDelegatePrice": "120000.0",      // 止盈委托价
                        "stopDelegateOrderType": "MARKET",      // 止损委托订单类型
                        "stopDelegateTimeInForce": "GTC",       // 止损委托有效方式
                        "stopDelegatePrice": "100000.0",        // 止损委托价
                        "closeType": "ALL",                     // 平仓类型:ALL(全仓);FIXED(部分仓位)
                        "state": "NOT_TRIGGERED",               // 状态
                        "desc": "",                             // 描述
                        "triggerPriceSide": "UP",               // 触发价方向
                        "createdTime": 1731231231000,           // 创建时间(ms)
                        "updatedTime": 1731231231000,           // 更新时间(ms)
                        "leverage": 20,                         // 杠杆倍数
                        "entryPrice": "107577.0",               // 开仓均价
                        "positionSize": "0.5",                  // 持仓数量（标的币）
                        "isolatedMargin": "21.59097358",        // 逐仓保证金
                        "positionType": "ISOLATED",             // 仓位类型:CROSSED;ISOLATED
                        "sourceType": "DEFAULT",                // 来源类型
                        "sourceId": "556931318219000000",       // 来源id
                        "fixedPositionInfo": {                  // 仅 FIXED 平仓类型出现
                            "profitFixedLatest": {              // 最新的部分仓位止盈止损（无则为空对象 {}）
                                "profitId": "556931318219666114",
                                "triggerPriceType": "LATEST_PRICE",
                                "triggerProfitPrice": "121000.0",
                                "triggerStopPrice": "99000.0"
                            },
                            "profitFixedCount": 2               // 部分仓位止盈止损总数
                        }
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

---
title: 计划委托
position_number: 12
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
           "entrust"
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
                "ch": "entrust",
                "data": {
                        "entrustId": "556931318219666113",   // 计划委托id
                        "symbol": "btc_usdt",                // 交易对
                        "entrustType": "PROFIT",             // 委托类型
                        "orderSide": "BUY",                  // 买卖方向 BUY, SELL
                        "positionSide": "LONG",              // LONG, SHORT
                        "timeInForce": "GTC",                // 有效方式
                        "price": "107500.0",                 // 下单价格
                        "origQty": "0.5",                    // 下单数量（标的币）
                        "stopPrice": "108000.0",             // 触发价
                        "triggerPriceType": "LATEST_PRICE",  // 触发价格类型
                        "type": "ENTRUST",                   // 固定值 ENTRUST
                        "state": "NOT_TRIGGERED",            // 委托状态
                        "createdTime": 1731231231000,        // 创建时间(ms)
                        "updatedTime": 1731231231000,        // 更新时间(ms)
                        "delegateTriggerPriceType": "LATEST_PRICE", // 委托触发价格类型
                        "triggerProfitPrice": "120000.0",    // 止盈触发价
                        "triggerStopPrice": "100000.0",      // 止损触发价
                        "profitDelegateOrderType": "MARKET", // 止盈委托订单类型
                        "profitDelegateTimeInForce": "GTC",  // 止盈委托有效方式
                        "profitDelegatePrice": "120000.0",   // 止盈委托价
                        "stopDelegateOrderType": "MARKET",   // 止损委托订单类型
                        "stopDelegateTimeInForce": "GTC",    // 止损委托有效方式
                        "stopDelegatePrice": "100000.0",     // 止损委托价
                        "clientOrderId": "123456",           // 自定义订单id
                        "orderType": "LIMIT",                // 订单类型 [LIMIT;MARKET]
                        "sourceType": 0                      // 来源类型
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

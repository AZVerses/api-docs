---
title: 用户订单
position_number: 10
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
           "order"
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
                    "ch": "order",
                    "data": {
                         "symbol":"btc_usdt",         // 交易对
                         "orderId": "1234",           // 订单id
                         "clientOrderId": "123456",   // 自定义订单id
                         "origQty": "0.5",            // 下单数量（标的币）
                         "avgPrice": "107577.0",      // 成交均价
                         "executedQty":"0.5",         // 已成交数量（标的币）
                         "positionSide": "LONG",      // LONG, SHORT
                         "marginFrozen":"123",        // 占用保证金
                         "state": "FILLED",           // 订单状态 NEW:新建;未成交;PARTIALLY_FILLED:部分成交;PARTIALLY_CANCELED:部分撤销;FILLED:全部成交;CANCELED:已撤销;REJECTED:下单失败;EXPIRED:已过期
                         "sourceType":"DEFAULT",      // DEFAULT:普通订单;ENTRUST:计划委托;PROFIT:止盈止损
                         "price": "107500.0",         // 下单价格
                         "orderSide": "BUY",          // 买卖方向
                         "timeInForce": "GTC",        // 有效方式
                         "orderType": "MARKET",       // 订单类型 LIMIT:限价, MARKET:市价
                         "lastTradeId": "556931318219666113", // 最后一次成交id
                         "sourceId": "556931318219000000",    // 来源id（计划委托/止盈止损订单id，适用时）
                         "leverage":20,               // 杠杆倍数
                         "positionType": "ISOLATED",  // 仓位类型：CROSSED（全仓）;ISOLATED（逐仓）
                         "isProfit": true,            // 是否止盈止损单；以下字段仅在 true 时出现
                         "triggerPriceType": "LATEST_PRICE",     // 触发价格类型
                         "profitDelegateOrderType": "MARKET",    // 止盈委托订单类型
                         "profitDelegateTimeInForce": "GTC",     // 止盈委托有效方式
                         "stopDelegateOrderType": "MARKET",      // 止损委托订单类型
                         "stopDelegateTimeInForce": "GTC",       // 止损委托有效方式
                         "triggerProfitPrice": "120000.0",       // 止盈触发价
                         "profitDelegatePrice": "120000.0",      // 止盈委托价
                         "triggerStopPrice": "100000.0",         // 止损触发价
                         "stopDelegatePrice": "100000.0",        // 止损委托价
                         "createdTime": 1731231231000,           // 下单时间(ms)
                         "updatedTime": 1731231231000            // 更新时间(ms)
                       },
                    "ts": 1731231231000
                }
        title: Response
        language: json
---

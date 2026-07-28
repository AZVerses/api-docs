---
title: 反手计划委托
position_number: 16
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
           "plan_reverse_entrust"
        ],
       "id": "{id}"
    }
  ```

  该频道推送反手（反方向）计划委托。数据结构与 `entrust` 频道一致，`sourceType` = `7`（REVERSE_PLAN）。

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "plan_reverse_entrust",
                "data": {
                        "entrustId": "556931318219666113",   // 计划委托id
                        "symbol": "btc_usdt",                // 交易对
                        "entrustType": "PLAN",               // 委托类型
                        "orderSide": "SELL",                 // 买卖方向 BUY, SELL
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
                        "clientOrderId": "123456",           // 自定义订单id
                        "orderType": "LIMIT",                // 订单类型 [LIMIT;MARKET]
                        "sourceType": 7                      // 来源类型（7 = REVERSE_PLAN）
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

---
title: Reverse plan entrust
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

  This channel carries reverse (opposite-direction) plan orders. The payload shares the same shape as the `entrust` channel, with `sourceType` = `7` (REVERSE_PLAN).

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
                        "entrustId": "556931318219666113",   // Entrust (plan order) ID
                        "symbol": "btc_usdt",                // Trading pair
                        "entrustType": "PLAN",               // Entrust type
                        "orderSide": "SELL",                 // BUY, SELL
                        "positionSide": "LONG",              // LONG, SHORT
                        "timeInForce": "GTC",                // Time in force
                        "price": "107500.0",                 // Order price
                        "origQty": "0.5",                    // Original quantity (base coin)
                        "stopPrice": "108000.0",             // Trigger (stop) price
                        "triggerPriceType": "LATEST_PRICE",  // Trigger price type
                        "type": "ENTRUST",                   // Fixed value ENTRUST
                        "state": "NOT_TRIGGERED",            // Entrust state
                        "createdTime": 1731231231000,        // Create time (ms)
                        "updatedTime": 1731231231000,        // Update time (ms)
                        "clientOrderId": "123456",           // Client order ID
                        "orderType": "LIMIT",                // Order type [LIMIT;MARKET]
                        "sourceType": 7                      // Source type (7 = REVERSE_PLAN)
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

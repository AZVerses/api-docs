---
title: Plan entrust
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
                        "entrustId": "556931318219666113",   // Entrust (plan order) ID
                        "symbol": "btc_usdt",                // Trading pair
                        "entrustType": "PROFIT",             // Entrust type
                        "orderSide": "BUY",                  // BUY, SELL
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
                        "delegateTriggerPriceType": "LATEST_PRICE", // Delegate trigger price type
                        "triggerProfitPrice": "120000.0",    // Take-profit trigger price
                        "triggerStopPrice": "100000.0",      // Stop-loss trigger price
                        "profitDelegateOrderType": "MARKET", // Take-profit delegate order type
                        "profitDelegateTimeInForce": "GTC",  // Take-profit delegate time in force
                        "profitDelegatePrice": "120000.0",   // Take-profit delegate price
                        "stopDelegateOrderType": "MARKET",   // Stop-loss delegate order type
                        "stopDelegateTimeInForce": "GTC",    // Stop-loss delegate time in force
                        "stopDelegatePrice": "100000.0",     // Stop-loss delegate price
                        "clientOrderId": "123456",           // Client order ID
                        "orderType": "LIMIT",                // Order type [LIMIT;MARKET]
                        "sourceType": 0                      // Source type
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

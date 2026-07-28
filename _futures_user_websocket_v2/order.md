---
title: user Order
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
                         "symbol":"btc_usdt",         // Trading pair
                         "orderId": "1234",           // Order ID
                         "clientOrderId": "123456",   // Client order ID
                         "origQty": "0.5",            // Original quantity (base coin)
                         "avgPrice": "107577.0",      // Average filled price
                         "executedQty":"0.5",         // Filled quantity (base coin)
                         "positionSide": "LONG",      // LONG, SHORT
                         "marginFrozen":"123",        // Occupied margin
                         "state": "FILLED",           // state:NEW(unfilled);PARTIALLY_FILLED;PARTIALLY_CANCELED;FILLED;CANCELED;REJECTED;EXPIRED
                         "sourceType":"DEFAULT",      // DEFAULT:normal order;ENTRUST:plan order;PROFIT:take profit / stop loss
                         "price": "107500.0",         // Order price
                         "orderSide": "BUY",          // BUY, SELL
                         "timeInForce": "GTC",        // Time in force
                         "orderType": "MARKET",       // Order type [LIMIT;MARKET]
                         "lastTradeId": "556931318219666113", // Last trade ID
                         "sourceId": "556931318219000000",    // Source ID (entrust/profit order id, when applicable)
                         "leverage":20,               // Leverage
                         "positionType": "ISOLATED",  // Position type:CROSSED;ISOLATED
                         "isProfit": true,            // Whether this is a TP/SL order; the fields below are present only when true
                         "triggerPriceType": "LATEST_PRICE",     // Trigger price type
                         "profitDelegateOrderType": "MARKET",    // Take-profit delegate order type
                         "profitDelegateTimeInForce": "GTC",     // Take-profit delegate time in force
                         "stopDelegateOrderType": "MARKET",      // Stop-loss delegate order type
                         "stopDelegateTimeInForce": "GTC",       // Stop-loss delegate time in force
                         "triggerProfitPrice": "120000.0",       // Take-profit trigger price
                         "profitDelegatePrice": "120000.0",      // Take-profit delegate price
                         "triggerStopPrice": "100000.0",         // Stop-loss trigger price
                         "stopDelegatePrice": "100000.0",        // Stop-loss delegate price
                         "createdTime": 1731231231000,           // Create time (ms)
                         "updatedTime": 1731231231000            // Update time (ms)
                       },
                    "ts": 1731231231000
                }
        title: Response
        language: json
---

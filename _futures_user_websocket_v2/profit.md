---
title: Take profit / stop loss
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
                        "profitId": "556931318219666113",       // TP/SL ID
                        "symbol": "btc_usdt",                   // Trading pair
                        "positionSide": "LONG",                 // LONG, SHORT
                        "origQty": "0.5",                       // Original quantity (base coin)
                        "triggerPriceType": "LATEST_PRICE",     // Trigger price type
                        "triggerProfitPrice": "120000.0",       // Take-profit trigger price
                        "triggerStopPrice": "100000.0",         // Stop-loss trigger price
                        "profitDelegateOrderType": "MARKET",    // Take-profit delegate order type
                        "profitDelegateTimeInForce": "GTC",     // Take-profit delegate time in force
                        "profitDelegatePrice": "120000.0",      // Take-profit delegate price
                        "stopDelegateOrderType": "MARKET",      // Stop-loss delegate order type
                        "stopDelegateTimeInForce": "GTC",       // Stop-loss delegate time in force
                        "stopDelegatePrice": "100000.0",        // Stop-loss delegate price
                        "closeType": "ALL",                     // Close type:ALL(all position);FIXED(partial position)
                        "state": "NOT_TRIGGERED",               // State
                        "desc": "",                             // Description
                        "triggerPriceSide": "UP",               // Trigger price side
                        "createdTime": 1731231231000,           // Create time (ms)
                        "updatedTime": 1731231231000,           // Update time (ms)
                        "leverage": 20,                         // Leverage
                        "entryPrice": "107577.0",               // Open position average price
                        "positionSize": "0.5",                  // Position quantity (base coin)
                        "isolatedMargin": "21.59097358",        // Isolated margin
                        "positionType": "ISOLATED",             // Position type:CROSSED;ISOLATED
                        "sourceType": "DEFAULT",                // Source type
                        "sourceId": "556931318219000000",       // Source ID
                        "fixedPositionInfo": {                  // Present only for FIXED close type
                            "profitFixedLatest": {              // Latest partial-position TP/SL (empty {} when none)
                                "profitId": "556931318219666114",
                                "triggerPriceType": "LATEST_PRICE",
                                "triggerProfitPrice": "121000.0",
                                "triggerStopPrice": "99000.0"
                            },
                            "profitFixedCount": 2               // Total number of partial-position TP/SL
                        }
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

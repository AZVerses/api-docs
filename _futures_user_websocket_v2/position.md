---
title: Change position
position_number: 8
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
           "position"
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
                "ch": "position",
                "data": {
                            "accountId": 8654006125462,
                            "accountType": 0,
                            "symbol": "btc_usdt",
                            "contractType": "PERPETUAL",    // PERPETUAL, DELIVERY
                            "positionType": "CROSSED",      // ISOLATED, CROSSED
                            "positionSide": "LONG",
                            "positionSize": "0.2",          // Position quantity (base coin)
                            "closeOrderSize": "0",          // Close pending-order quantity (base coin)
                            "availableCloseSize": "0.2",    // Available close quantity (base coin)
                            "realizedProfit": "-113.4475",  // Realized profit and loss
                            "entryPrice": "107577.0",       // Open position average price
                            "openOrderSize": "0",           // Open-order occupied quantity (base coin)
                            "isolatedMargin": "21.59097358",       // Isolated margin
                            "openOrderMarginFrozen": "0.00000000", // Occupied open-position margin
                            "underlyingType": "U_BASED",    // COIN_BASED, U_BASED
                            "leverage": 10,                 // Leverage
                            "state": 1,                     // Position state
                            "closeProfit": "232.7172",      // Closed profit and loss
                            "totalFee": "-133.1456",        // Total fee
                            "totalFundFee": "-213.0191",    // Total funding fee
                            "markPrice": "106208.1",        // Mark price
                            "marginCoin": "usdt",           // Margin coin
                            "profitId": "556931318219666113",   // All-position TP/SL profit id (null when none)
                            "triggerPriceType": "LATEST_PRICE", // All-position TP/SL trigger price type
                            "triggerProfitPrice": "120000.0",   // All-position take-profit trigger price
                            "triggerStopPrice": "100000.0",     // All-position stop-loss trigger price
                            "profitFixedLatest": {              // Latest partial-position TP/SL (empty {} when none)
                                "profitId": "556931318219666114",
                                "triggerPriceType": "LATEST_PRICE",
                                "triggerProfitPrice": "121000.0",
                                "triggerStopPrice": "99000.0"
                            },
                            "profitFixedCount": 2,          // Total number of partial-position TP/SL
                            "updatedTime": 1762184243057
                   },
                "ts": 1762184243057
            }
        title: Response
        language: json
---

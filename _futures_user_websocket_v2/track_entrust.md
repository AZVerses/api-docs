---
title: Trailing stop entrust
position_number: 14
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
           "track_entrust"
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
                "ch": "track_entrust",
                "data": {
                        "trackId": "556931318219666113",     // Trailing entrust ID
                        "symbol": "btc_usdt",                // Trading pair
                        "orderSide": "BUY",                  // BUY, SELL
                        "positionSide": "LONG",              // LONG, SHORT
                        "configActivation": true,            // Whether an activation price is configured
                        "activationPrice": "108000.0",       // Activation price
                        "currentPrice": "107800.0",          // Current price
                        "origQty": "0.5",                    // Original quantity (base coin)
                        "stopPrice": "107000.0",             // Stop price
                        "triggerPriceType": "LATEST_PRICE",  // Trigger price type
                        "callback": "RATE",                  // Callback type
                        "callbackVal": "0.01",               // Callback value
                        "state": "NOT_TRIGGERED",            // State
                        "desc": "",                          // Description
                        "createdTime": 1731231231000,        // Create time (ms)
                        "updatedTime": 1731231231000         // Update time (ms)
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

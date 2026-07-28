---
title: Transactions
position_number: 9
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
           "trade"
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
                "ch": "trade",
                "data": {
                        "id": "556931318219666113",
                        "symbol": "btc_usdt",       // Symbol
                        "orderSide": "BUY",         // Order side
                        "positionSide": "LONG",     // Position side
                        "orderId":"12312312",       // Order ID
                        "price":"34244",            // Price
                        "quantity":"0.5",           // Quantity (base coin)
                        "isMaker": true,            // Is maker or not, true:maker;false:taker
                        "marginUnfrozen":"123",     // Quantity of unfrozen margin
                        "fee": "0.0002",            // Fee (string)
                        "timestamp":1731231231000,  // Timestamp (ms)
                        "clientOrderId":"123456",   // Client order ID
                        "oppositeUserId": "1234",   // Opposite user id, provided for market makers / vault accounts only
                        "oppositeOrderId": "2345",  // Opposite order id, provided for market makers / vault accounts only
                        "execId": "123",            // Execution id, provided for market makers / vault accounts only
                        "searchId": "789"           // Search id, provided for market makers / vault accounts only
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

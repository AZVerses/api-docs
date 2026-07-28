---
title: Get spot + perp asset detail
position_number: 4
type: get
description: /az/spot/balance/detail
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    Aggregated asset detail: converted summary + per-currency spot detail + per-currency perp detail.
left_code_blocks:
    -
        code_block:
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                    "summary": {
                      "totalValue": "0",           //total assets converted to USDT
                      "spotBalance": "0",          //spot balance converted to USDT
                      "perpsBalance": "0",         //perp balance converted to USDT (incl. unrealized PnL)
                      "perpsWalletBalance": "0",   //perp wallet balance converted to USDT
                      "perpsBotBalance": "0",      //perp strategy-bot balance converted to USDT
                      "vaultBalance": "0",         //vault balance converted to USDT (incl. unrealized PnL)
                      "predictBalance": "0",       //prediction-market unsettled position valuation converted to USDT
                      "unrealizedPnl": "0",        //perp unrealized PnL (USDT)
                      "availableAmount": "0"       //available balance (USDT)
                    },
                    "spotDetails": [
                      {
                        "currency": "usdt",
                        "currencyId": 0,
                        "frozenAmount": "0",       //unavailable (freeze + lock + copy-trade + order + withdraw)
                        "freeze": "0",             //freeze
                        "lock": "0",               //lock
                        "trade": "0",              //order (entrust)
                        "withdraw": "0",           //withdraw
                        "availableAmount": "0",    //available amount
                        "totalAmount": "0",        //total amount
                        "convertBtcAmount": "0",   //converted BTC amount
                        "convertUsdtAmount": "0",  //converted USDT amount
                        "convertAvailableUsdtAmount": "0"  //converted USDT available amount
                      }
                    ],
                    "perpDetails": [
                      {
                        "accountId": 0,
                        "userId": 0,
                        "coin": "usdt",            //settlement coin
                        "underlyingType": 1,       //underlying type (U-based / coin-based)
                        "walletBalance": "0",      //wallet balance
                        "openOrderMarginFrozen": "0",  //open-order margin frozen
                        "isolatedMargin": "0",     //isolated margin
                        "amount": "0",             //available amount
                        "totalAmount": "0",        //total amount
                        "profit": "0",             //realized profit
                        "notProfit": "0"           //unrealized profit
                      }
                    ]
                  }
                }
        title: Response
        language: json
---


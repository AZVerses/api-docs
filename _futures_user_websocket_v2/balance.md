---
title: Balance change
position_number: 7
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
                 "balance"
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
                "ch": "balance",
                "data": {
                          "coin": "usdt",                             //Currency
                          "underlyingType": 2,                        //1:Coin-M,2:USDT-M
                          "walletBalance": "9652.09217635",           //Balance
                          "openOrderMarginFrozen": "0.00000000",      //Isolated order frozen margin
                          "isolatedMargin": "0",                      //Isolated margin
                          "crossedMargin": "0",                       //Crossed margin (always 0; see virtualCrossMargin)
                          "availableBalance": "9613.51195739",        //Available balance
                          "virtualCrossMargin": "38.58021896",        //Virtual crossed margin (usdt only, otherwise 0)
                          "virtualOpenOrderMarginFrozen": "0.00000000", //Virtual crossed open-order frozen margin (usdt only, otherwise 0)
                          "virtualCrossNotProfit": "0"                //Virtual crossed unrealized PnL
                   },
                "ts": 1762184243057
            }
        title: Response
        language: json
---

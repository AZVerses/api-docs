---
title: ticker
position_number: 11
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
    **request**

    format: ticker@\{symbol\}

    eg: ticker@btc\_usdt

    rate: real

    ticker has absorbed the best bid/ask (`bp/bq/ap/aq`); there is no separate `agg_ticker` channel. Spot ticker does not carry `ix`/`mx` (index/mark price are futures-only).
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "ticker@btc_usdt", // channel
                    "s": "btc_usdt",         // symbol
                    "o": "30000",            // open price
                    "c": "39000",            // close price (last price)
                    "h": "38000",            // highest price
                    "l": "40000",            // lowest price
                    "v": "4",                // quantity (base)
                    "uv": "150000",          // volume (quote)
                    "r": "-0.02",            // price change rate
                    "bp": "38999",           // bid one price
                    "bq": "1.2",             // bid one quantity
                    "ap": "39001",           // ask one price
                    "aq": "0.8",             // ask one quantity
                    "ts": 1657586700119      // time (ms)
                }
        title: Response
        language: json
---

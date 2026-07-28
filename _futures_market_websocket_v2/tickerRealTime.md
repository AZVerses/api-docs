---
title: Ticker
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
    **request**

    format: ticker@\{symbol\}

    eg: ticker@btc\_usdt

    rate: real

    ticker has absorbed the best bid/ask (`bp/bq/ap/aq`); there is no separate `agg_ticker` channel. Futures ticker also carries `ix` (index price) and `mx` (mark price).
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
                    "o": "109927.8",         // open price
                    "c": "109822.7",         // close price (last price)
                    "h": "114308.1",         // highest price
                    "l": "108600.0",         // lowest price
                    "v": "1877436",          // quantity (base)
                    "uv": "20640737.33039",  // volume (quote)
                    "r": "-0.0009",          // price change rate
                    "bp": "109822.6",        // bid one price
                    "bq": "1.2",             // bid one quantity
                    "ap": "109822.8",        // ask one price
                    "aq": "0.8",             // ask one quantity
                    "ix": "109820.0",        // index price
                    "mx": "109821.5",        // mark price
                    "ts": 1762007085988      // time (ms)
                }
        title: Response
        language: json
---

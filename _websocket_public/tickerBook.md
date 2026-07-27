---
title: ticker book
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

    format: tickerbook@\{symbol\}

    eg: tickerbook@btc\_usdt

    rate: real

    Best bid/ask (top-of-book) changes only. `u` is the matching updateId.
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "tickerbook@btc_usdt", // channel
                    "s": "btc_usdt",             // symbol
                    "u": 128346,                 // matching updateId
                    "bp": "64000.5",             // bid one price
                    "bq": "1.23",                // bid one quantity
                    "ap": "64001.0",             // ask one price
                    "aq": "0.88",                // ask one quantity
                    "ts": 1657586700119          // time (ms)
                }
        title: Response
        language: json
---

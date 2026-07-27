---
title: K-line
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
    **request**

    &nbsp;

    format: kline\_\{interval\}@\{symbol\}

    interval: 1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1d, 2d, 3d, 1w, 1M

    eg: kline\_5m@btc\_usdt

    rate: real

    &nbsp;
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "kline_5m@btc_usdt", // channel
                    "s": "btc_usdt",           // symbol
                    "p": "last",               // price type (spot is always last)
                    "o": "44000",              // open price
                    "c": "50000",              // close price
                    "h": "52000",              // highest price
                    "l": "36000",              // lowest price
                    "v": "34.2",               // quantity (base)
                    "uv": "230000",            // volume (quote)
                    "i": "5m",                 // interval
                    "t": 1656043200000         // start time (ms)
                }
        title: Response
        language: json
---

---
title: K-line
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
    **request**

    &nbsp;

    format: kline\_\{interval\}@\{symbol\}

    interval: 1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1d, 3d, 1w, 1M

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
                    "p": "last",               // price type (last)
                    "o": "110096.3",           // open price
                    "c": "109933.6",           // close price
                    "h": "110164.4",           // highest price
                    "l": "109654.6",           // lowest price
                    "v": "122187",             // quantity (base)
                    "uv": "1344027.60259",     // volume (quote)
                    "i": "5m",                 // interval
                    "t": 1761998400000         // start time (ms)
                }
        title: Response
        language: json
---

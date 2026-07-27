---
title: Subscription parameters
position_number: 6
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
    **format**

    `<type>@<symbol>` , where `<symbol>` is lowercase underscore (e.g. `btc_usdt`).

    Examples: `ticker@btc_usdt` , `depth@btc_usdt` , `depth20@btc_usdt` , `tickerbook@btc_usdt` , `deal@btc_usdt` , `kline_1m@btc_usdt` .

    The full-market channel `tickers` has no `@symbol` suffix.
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

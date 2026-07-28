---
title: 订阅参数
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
    **结构**

    `<type>@<symbol>` ，其中 `<symbol>` 用小写下划线（如 `btc_usdt`）。

    示例：`ticker@btc_usdt` 、`depth@btc_usdt` 、`depth20@btc_usdt` 、`tickerbook@btc_usdt` 、`deal@btc_usdt` 、`kline_1m@btc_usdt` 、`fundrate@btc_usdt` 、`index_price@btc_usdt` 、`mark_price@btc_usdt` 。

    全市场频道 `tickers` 无 `@symbol` 后缀。
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

---
title: K线
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
    **请求**

    &nbsp;

    语法: kline\_\{interval\}@\{symbol\}

    interval: 1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1d, 3d, 1w, 1M

    示例: kline\_5m@btc\_usdt

    速率: 实时

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
                    "ch": "kline_5m@btc_usdt", // 频道
                    "s": "btc_usdt",           // symbol 交易对
                    "p": "last",               // 价格类型(last)
                    "o": "110096.3",           // open 开盘价
                    "c": "109933.6",           // close 收盘价
                    "h": "110164.4",           // high 最高价
                    "l": "109654.6",           // low 最低价
                    "v": "122187",             // 成交量(base)
                    "uv": "1344027.60259",     // 成交额(quote)
                    "i": "5m",                 // interval 间隔
                    "t": 1761998400000         // 起始时间(ms)
                }
        title: Response
        language: json
---

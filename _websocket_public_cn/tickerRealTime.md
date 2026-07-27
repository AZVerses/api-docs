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
    **请求**

    语法: ticker@\{symbol\}

    示例: ticker@btc\_usdt

    速率: 实时

    ticker 已吸收最优买卖一价量（`bp/bq/ap/aq`），无独立 `agg_ticker` 频道。现货 ticker 不含 `ix`/`mx`（指数/标记价为合约专属）。
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "ticker@btc_usdt", // 频道
                    "s": "btc_usdt",         // symbol 交易对
                    "o": "30000",            // open 第一笔
                    "c": "39000",            // close 最后一笔(最新价)
                    "h": "38000",            // high 最高价
                    "l": "40000",            // low 最低价
                    "v": "4",                // 成交量(base)
                    "uv": "150000",          // 成交额(quote)
                    "r": "-0.02",            // 涨跌幅
                    "bp": "38999",           // 买一价
                    "bq": "1.2",             // 买一量
                    "ap": "39001",           // 卖一价
                    "aq": "0.8",             // 卖一量
                    "ts": 1657586700119      // 时间(ms)
                }
        title: Response
        language: json
---

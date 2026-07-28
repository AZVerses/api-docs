---
title: ticker
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
    **请求**

    语法: ticker@\{symbol\}

    示例: ticker@btc\_usdt

    速率: 实时

    ticker 已吸收最优买卖一价量（`bp/bq/ap/aq`），无独立 `agg_ticker` 频道。合约 ticker 另带 `ix`（指数价）与 `mx`（标记价）。
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
                    "o": "109927.8",         // open 第一笔
                    "c": "109822.7",         // close 最后一笔(最新价)
                    "h": "114308.1",         // high 最高价
                    "l": "108600.0",         // low 最低价
                    "v": "1877436",          // 成交量(base)
                    "uv": "20640737.33039",  // 成交额(quote)
                    "r": "-0.0009",          // 涨跌幅
                    "bp": "109822.6",        // 买一价
                    "bq": "1.2",             // 买一量
                    "ap": "109822.8",        // 卖一价
                    "aq": "0.8",             // 卖一量
                    "ix": "109820.0",        // 指数价
                    "mx": "109821.5",        // 标记价
                    "ts": 1762007085988      // 时间(ms)
                }
        title: Response
        language: json
---

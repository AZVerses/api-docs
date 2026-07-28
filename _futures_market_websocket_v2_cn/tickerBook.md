---
title: ticker盘口
position_number: 13
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

    语法: tickerbook@\{symbol\}

    示例: tickerbook@btc\_usdt

    速率: 实时

    盘口最优价变化（仅买卖一价量）；替代旧的 `best_price` 频道。`u` 为撮合 updateId。
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "tickerbook@btc_usdt", // 频道
                    "s": "btc_usdt",             // symbol
                    "u": 128346,                 // 撮合 updateId
                    "bp": "64000.5",             // 买一价
                    "bq": "1.23",                // 买一量
                    "ap": "64001.0",             // 卖一价
                    "aq": "0.88",                // 卖一量
                    "ts": 1657586700119          // 时间(ms)
                }
        title: Response
        language: json
---

---
title: 全市场ticker
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

    语法: tickers

    （无 `@symbol` 后缀；全市场批量快照）

    速率: 每 ~3s 推一帧全市场快照；订阅即先发一帧。

    `data` 每元素字段与单个 `ticker` 帧一致（无 `ch`）。
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "tickers",
                    "data": [
                        {
                            "s": "btc_usdt",
                            "o": "30000",
                            "c": "39000",
                            "h": "38000",
                            "l": "40000",
                            "v": "4",
                            "uv": "150000",
                            "r": "-0.02",
                            "bp": "38999",
                            "bq": "1.2",
                            "ap": "39001",
                            "aq": "0.8",
                            "ts": 1657586700119
                        },
                        {
                            "s": "eth_usdt",
                            "o": "...", "c": "...", "h": "...", "l": "...",
                            "v": "...", "uv": "...", "r": "...",
                            "bp": "...", "bq": "...", "ap": "...", "aq": "...",
                            "ts": 1657586700119
                        }
                    ]
                }
        title: Response
        language: json
---

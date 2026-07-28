---
title: 全市场ticker
position_number: 14
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

    `data` 每元素字段与单个 `ticker` 帧一致（无 `ch`），含合约专属的 `ix`（指数价）与 `mx`（标记价）。
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
                            "o": "109927.8",
                            "c": "109822.7",
                            "h": "114308.1",
                            "l": "108600.0",
                            "v": "1877436",
                            "uv": "20640737.33039",
                            "r": "-0.0009",
                            "bp": "109822.6",
                            "bq": "1.2",
                            "ap": "109822.8",
                            "aq": "0.8",
                            "ix": "109820.0",
                            "mx": "109821.5",
                            "ts": 1762007085988
                        },
                        {
                            "s": "eth_usdt",
                            "o": "...", "c": "...", "h": "...", "l": "...",
                            "v": "...", "uv": "...", "r": "...",
                            "bp": "...", "bq": "...", "ap": "...", "aq": "...",
                            "ix": "...", "mx": "...",
                            "ts": 1762007085988
                        }
                    ]
                }
        title: Response
        language: json
---

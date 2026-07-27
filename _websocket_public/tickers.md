---
title: All market tickers
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
    **request**

    format: tickers

    (no `@symbol` suffix; full-market batch snapshot)

    rate: a full-market snapshot every ~3s; one frame is pushed immediately on subscribe.

    Each element of `data` has the same fields as a single `ticker` frame (without `ch`).
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

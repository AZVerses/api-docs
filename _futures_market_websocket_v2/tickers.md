---
title: All market tickers
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
    **request**

    format: tickers

    (no `@symbol` suffix; full-market batch snapshot)

    rate: a full-market snapshot every ~3s; one frame is pushed immediately on subscribe.

    Each element of `data` has the same fields as a single `ticker` frame (without `ch`), including the futures-only `ix` (index price) and `mx` (mark price).
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

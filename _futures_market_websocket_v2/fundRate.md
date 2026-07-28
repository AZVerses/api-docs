---
title: Fund rate
position_number: 17
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

    format: fundrate@\{symbol\}

    eg: fundrate@btc\_usdt

    rate: 60s
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "fundrate@btc_usdt", // channel
                    "s": "btc_usdt",           // symbol
                    "r": "0.0001",             // funding rate
                    "t": 1655992403617,        // time (ms)
                    "nt": 1655996003617        // next funding time (ms)
                }
        title: Response
        language: json
---

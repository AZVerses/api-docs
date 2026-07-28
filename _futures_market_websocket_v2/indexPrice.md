---
title: Index price
position_number: 15
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

    format: index_price@\{symbol\}

    eg: index_price@btc\_usdt

    rate: once per second (1000ms)

    This is a flat `ch` frame (same as the other channels); the price is pushed strictly once per second.
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "index_price@btc_usdt", // channel
                    "s": "btc_usdt",              // trading pair
                    "p": "63601.87",              // index price
                    "t": 1785221435078            // timestamp
                }
        title: Response
        language: json
---

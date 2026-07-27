---
title: Trade record
position_number: 8
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

    format: deal@\{symbol\}

    eg: deal@btc\_usdt

    rate: real
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "deal@btc_usdt",   //channel
                "s": "btc_usdt",         //symbol
                "p": "43000",            //price
                "a": "0.21",             //quantity (base)
                "m": "BID",              //taker side: BID or ASK
                "t": 1655992403617       //time
            }
        title: Response
        language: json
---

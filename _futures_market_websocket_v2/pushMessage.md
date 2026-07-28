---
title: Push message format
position_number: 4
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
    Push frames are flat and carry a `ch` field identifying the channel (`<type>@<symbol>`). Field keys are short keys. Note the full-depth channel adds a `type` (snapshot/delta) field; see the depth channels. The `index_price` / `mark_price` channels are the exception and keep the legacy `{topic,event,data}` envelope.
left_code_blocks:
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
        title: format
        language: javascript
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "deal@btc_usdt",
                    "s": "btc_usdt",
                    "p": "43000",
                    "a": "0.21",
                    "m": "BID",
                    "t": 1655992403617
                }
        title: Example of transaction record (real-time push message)
        language: json
---

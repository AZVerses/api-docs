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

    This channel keeps the legacy `{topic,event,data}` envelope (it is not a flat `ch` frame).
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "topic": "index_price", 
                    "event": "index_price@btc_usdt", 
                    "data": {
                        "s":"btc_usdt", //trading pair
                        "p":"50000",    //price
                        "t":123124124   //timestamp
                   }
                }
        title: Response
        language: json
---

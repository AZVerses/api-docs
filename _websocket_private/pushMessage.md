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
    Push frames are flat and carry a `ch` field identifying the channel, the `data` payload, and a `ts` server timestamp (epoch millisecond). Field keys inside `data` are short keys.
left_code_blocks:
    -
        code_block: |-
            {
                "ch": "balance",   //channel
                "data": { },       //payload (short keys)
                "ts": 1656043204763
            }
        title: format
        language: javascript
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

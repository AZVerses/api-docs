---
title: Request message format
position_number: 2
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
    **param format**

    \{topic\}@\{arg\},\{arg\},…
left_code_blocks:
    -
        code_block: |-
                {
                    "method": "subscribe", 
                    "params": [
                        "{topic}@{arg},{arg}",    //event
                        "{topic}@{arg}"
                    ], 
                    "id": "{id}"
                }
        title: subscribe
        language: javascript
    -
        code_block: |-
            {
                "method": "unsubscribe", 
                "params": [
                    "{topic}@{arg},{arg}",    //event
                    "{topic}@{arg}"
                ], 
                "id": "{id}"
            }
        title: unsubscribe
        language: javascript
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

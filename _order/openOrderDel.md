---
title: Cancel the current pending order
position_number: 9
type: delete
split: -------------------------------------
description: /az/spot/open-order
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair, if not filled in, represents all
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "SPOT, PREDICTION"
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: BUY,SELL
        ranges:
    -
        name: mode
        type: string
        mandatory: false
        default: CMD
        description: 'cancel mode: CMD (bulk cancel by command), ITERATOR (cancel one by one)'
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**

    10/s/apikey
    <br>
    Note: The parameters should be placed in the request body in the form of json
left_code_blocks:
    -
        code_block:
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {}
                }
        title: Response
        language: json
---

---
title: Limited depth
position_number: 9
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

    &nbsp;

    format: depth20@\{symbol\} / depth50@\{symbol\} / depth100@\{symbol\}

    (the level is part of the channel name; supported levels are 20 / 50 / 100)

    eg: depth20@btc\_usdt

    rate: real (the server throttles high-frequency symbols)

    Each frame is a full top-N snapshot (whole-book replace, no increments). `u` is the matching-engine updateId (a version marker, a different source from the full-depth channel's local `u`).
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "depth20@btc_usdt",  // channel
                    "u": 12345678,             // matching updateId (version marker)
                    "b": [                     // bids (buy order) [0]price [1]quantity
                        [
                            "32000",
                            "0.2"
                        ],
                        [
                            "31000",
                            "0.5"
                        ]
                    ],
                    "a": [                     // asks (sell order) [0]price [1]quantity
                        [
                            "34000",
                            "1.2"
                        ],
                        [
                            "34001",
                            "2.3"
                        ]
                    ],
                    "ts": 1657699200000        // time (ms)
                }
        title: Response
        language: json
---

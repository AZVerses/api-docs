---
title: Change of prediction position
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
    param

    format: pred_position

    eg: pred_position

    Spot-only channel. Pushes the prediction-market position for one market, carrying both the YES and NO legs. An empty avg-price leg is sent as `null`.
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "pred_position",
                "data": {
                    "a": 214628532255,    // accountId
                    "m": 100123,          // marketId
                    "t": 1656043204763,   // updated time
                    "yq": "10",           // YES quantity
                    "nq": "5",            // NO quantity
                    "fy": "1",            // YES frozen
                    "fn": "0",            // NO frozen
                    "yap": "0.62",        // YES avg price (null when zero)
                    "nap": "0.38",        // NO avg price (null when zero)
                    "ycb": "6.2",         // YES cost basis
                    "ncb": "1.9"          // NO cost basis
                },
                "ts": 1656043204763
            }
        title: push
        language: json
---

---
title: Change of order
position_number: 7
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

    format: order

    eg: order
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "order",
                    "data": {
                        "s": "btc_usdt",                // symbol
                        "bc": "btc",                    // base currency
                        "qc": "usdt",                   // quote currency
                        "t": 1656043204763,             // happened time
                        "ct": 1656043204663,            // create time
                        "i": "6216559590087220004",     // order id
                        "ci": "test123",                // client order id
                        "st": "PARTIALLY_FILLED",       // state NEW/PARTIALLY_FILLED/FILLED/CANCELED/REJECTED/EXPIRED
                        "sd": "BUY",                    // side BUY/SELL
                        "tp": "LIMIT",                  // type LIMIT/MARKET
                        "bt": "SPOT",                   // bizType
                        "oq": "4",                      // original quantity
                        "oqq": "48000",                 // original quote quantity
                        "eq": "2",                      // executed quantity
                        "lq": "2",                      // leaving quantity
                        "p": "4000",                    // price
                        "ap": "30000",                  // avg price
                        "f": "0.002"                    // fee
                    },
                    "ts": 1656043204763
                }
        title: push
        language: json
---

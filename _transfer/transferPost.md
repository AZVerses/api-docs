---
title: Transfer between user business systems
position_number: 1
type: post
description: /az/spot/balance/transfer
parameters:
    -
        name: bizId
        type: string
        mandatory: true
        default:
        description: Unique id for idempotent processing. Only letters, numbers, '-' and '_' are allowed (regex ^[A-Za-z0-9-_]+$)
        ranges: Maximum length is 128
    -
        name: from
        type: enum
        mandatory: true
        default:
        description: Fund transfer out account. from and to must not be equal (FUND_015), out-of-range value reports FUND_021
        ranges: SPOT / FUTURES_U
    -
        name: to
        type: enum
        mandatory: true
        default:
        description: Fund transfer in account. from and to must not be equal (FUND_015), out-of-range value reports FUND_021
        ranges: SPOT / FUTURES_U
    -
        name: currency
        type: string
        mandatory: true
        default:
        description: Currency name must be all lowercase (usdt,btc). Reports FUND_017 if the currency does not exist
        ranges:
    -
        name: amount
        type: bigDecimal
        mandatory: true
        default:
        description: Transfer amount. Must be a positive number; trailing zeros are stripped and precision is bounded by the currency maxPrecision (lower bound 10)
        ranges:

content_markdown: >-


left_code_blocks:
    -
        code_block: |-
            public String transferPost(){


            }
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
                  "mc": "SUCCESS",
                  "ma": [],
                  "result": 123456 //The returned unique id of the transfer, it is recommended to store it for reconciliation
                }
        title: Response
        language: json
---

---
title: 请求报文格式
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
content_markdown:
left_code_blocks:
    -
        code_block: |-
                {
                    "method": "subscribe",
                    "params": [
                        "ticker@btc_usdt",
                        "depth@btc_usdt"
                    ],
                    "id": 1              //回调ID
                }
        title: 订阅
        language: javascript
    -
        code_block: |-
                {
                    "method": "unsubscribe",
                    "params": [
                        "ticker@btc_usdt"
                    ],
                    "id": 2              //回调ID
                }
        title: 取消订阅
        language: javascript
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

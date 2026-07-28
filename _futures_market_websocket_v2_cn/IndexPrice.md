---
title: 指数价格
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
    **请求**

    语法: index_price@\{symbol\}

    示例: index_price@btc\_usdt

    速率: 每秒一次（1000ms）

    此频道为扁平 `ch` 帧（与其它频道一致），价格严格每秒下发。
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "index_price@btc_usdt", // 频道
                    "s": "btc_usdt",              // 交易对
                    "p": "63601.87",              // 指数价
                    "t": 1785221435078            // 时间戳
                }
        title: Response
        language: json
---

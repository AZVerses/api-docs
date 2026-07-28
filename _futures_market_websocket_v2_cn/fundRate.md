---
title: 资金费率
position_number: 17
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

    语法: fundrate@\{symbol\}

    示例: fundrate@btc\_usdt

    速率: 60s
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "fundrate@btc_usdt", // 频道
                    "s": "btc_usdt",           // symbol 交易对
                    "r": "0.0001",             // 资金费率
                    "t": 1655992403617,        // 时间(ms)
                    "nt": 1655996003617        // 下次资金费时间(ms)
                }
        title: Response
        language: json
---

---
title: 成交记录
position_number: 8
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

    语法: deal@\{symbol\}

    示例: deal@btc\_usdt

    速率: 实时
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "deal@btc_usdt",   //频道
                "s": "btc_usdt",         //symbol
                "p": "43000",            //价格
                "a": "0.21",             //数量(base)
                "m": "BID",              //taker方向: BID或ASK
                "t": 1655992403617       //时间
            }
        title: Response
        language: json
---

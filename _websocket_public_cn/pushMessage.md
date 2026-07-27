---
title: 推送报文格式
position_number: 4
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
    推送帧为扁平结构，带 `ch` 字段标识频道（`<type>@<symbol>`）。字段一律短键。注意全深度频道额外带 `type`（snapshot/delta）字段，详见深度频道。
left_code_blocks:
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
        title: 格式
        language: javascript
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "deal@btc_usdt",
                    "s": "btc_usdt",
                    "p": "43000",
                    "a": "0.21",
                    "m": "BID",
                    "t": 1655992403617
                }
        title: 成交记录(实时推送报文)样例
        language: json
---

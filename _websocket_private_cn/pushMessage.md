---
title: 推送报⽂格式
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
    推送帧为扁平结构，带 `ch` 标识频道、`data` 载荷、以及服务端时间戳 `ts`（epoch 毫秒）。`data` 内字段均为短键。
left_code_blocks:
    -
        code_block: |-
                {
                    "ch": "balance",   //频道
                    "data": { },       //数据（短键）
                    "ts": 1656043204763
                }
        title: 格式
        language: javascript
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

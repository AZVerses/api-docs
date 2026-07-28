---
title: 预测市场持仓变动
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

    语法: pred_position

    示例: pred_position

    现货专有频道。推送某个预测市场的持仓，同时携带 YES 与 NO 两腿。均价为 0 的一腿以 `null` 下发。
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
                    "a": 214628532255,    // accountId 账号
                    "m": 100123,          // marketId 市场ID
                    "t": 1656043204763,   // updatedTime 更新时间
                    "yq": "10",           // YES 持仓数量
                    "nq": "5",            // NO 持仓数量
                    "fy": "1",            // YES 冻结数量
                    "fn": "0",            // NO 冻结数量
                    "yap": "0.62",        // YES 成交均价（为 0 时 null）
                    "nap": "0.38",        // NO 成交均价（为 0 时 null）
                    "ycb": "6.2",         // YES 持仓成本
                    "ncb": "1.9"          // NO 持仓成本
                },
                "ts": 1656043204763
            }
        title: 推送
        language: json
---

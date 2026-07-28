---
title: 撤销当前挂单
position_number: 9
type: delete
split: -------------------------------------
description: /az/spot/open-order
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对，不传代表所有
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: >-
            业务类型  SPOT-现货, PREDICTION-预测市场
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: BUY-买,SELL-卖
        ranges:
    -
        name: mode
        type: string
        mandatory: false
        default: CMD
        description: '撤单模式：CMD-按指令批量撤销，ITERATOR-逐笔迭代撤销'
        ranges:
content_markdown: >-
    #### **限流规则**

    10/s/apikey
    <br>
    注意：参数以json形式放在body中
left_code_blocks:
    -
        code_block:
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
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {}
                }
        title: Response
        language: json
---

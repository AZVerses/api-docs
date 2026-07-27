---
title: 有限深度
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
    **请求**

    &nbsp;

    语法: depth20@\{symbol\} / depth50@\{symbol\} / depth100@\{symbol\}

    （档位并入频道名；支持 20 / 50 / 100）

    示例: depth20@btc\_usdt

    速率: 实时（服务端对高频 symbol 节流）

    每帧为该档位 top-N 全量（整本替换，无增量）。`u` 为撮合 updateId（版本标记，与全深度频道的本地 `u` 不同源）。
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "depth20@btc_usdt",  // 频道
                    "u": 12345678,             // 撮合 updateId(版本标记)
                    "b": [                     // bids 买盘 [0]价格 [1]数量
                        [
                            "32000",
                            "0.2"
                        ],
                        [
                            "31000",
                            "0.5"
                        ]
                    ],
                    "a": [                     // asks 卖盘 [0]价格 [1]数量
                        [
                            "34000",
                            "1.2"
                        ],
                        [
                            "34001",
                            "2.3"
                        ]
                    ],
                    "ts": 1657699200000        // 时间(ms)
                }
        title: Response
        language: json
---

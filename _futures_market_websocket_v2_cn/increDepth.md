---
title: 增量深度
position_number: 11
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

    语法: depth@\{symbol\}

    示例: depth@btc\_usdt

    速率: 订阅即下发快照，之后增量（~100ms）

    订阅即下发全量快照，之后推增量；服务端在重启 / 客户端落后时主动重发快照。无需 REST 拉快照、无需对齐撮合 updateId。

    * `u` = push 本地下发序列（per-symbol 单调 +1，**非**撮合 updateId）。

    * `pu` = 上一帧的 `u`（仅 delta 帧有；snapshot 无 `pu`）。

    * `b`/`a` 档 `[价, 量]`：`量 == "0"` 表示删除该档，否则 upsert。
left_code_blocks:
    -
        code_block: |-
                {
                    "ch": "depth@btc_usdt",
                    "type": "snapshot",
                    "u": 1024,
                    "b": [ ["32000","0.2"], ["31000","0.5"] ],
                    "a": [ ["34000","1.2"], ["34001","2.3"] ],
                    "ts": 1657699200000
                }
        title: snapshot
        language: json
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "depth@btc_usdt",    // 频道
                    "type": "delta",           // snapshot | delta
                    "u": 1025,                 // push 本地序列(+1)
                    "pu": 1024,                // 上一帧 u(仅 delta)
                    "b": [                     // bids [0]价 [1]量("0"=删档)
                        [
                            "32000",
                            "0"
                        ]
                    ],
                    "a": [                     // asks [0]价 [1]量
                        [
                            "34001",
                            "1.05"
                        ]
                    ],
                    "ts": 1657699200010        // 时间(ms)
                }
        title: delta
        language: json
---

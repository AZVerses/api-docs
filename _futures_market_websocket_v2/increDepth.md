---
title: Incremental depth
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
    **request**

    format: depth@\{symbol\}

    eg: depth@btc\_usdt

    rate: snapshot on subscribe, then deltas (~100ms)

    Subscribe pushes a full snapshot first, then deltas; the server actively re-pushes a snapshot on restart / when the client falls behind. No REST snapshot pull is needed and no matching-engine updateId alignment is needed.

    * `u` = push local sequence (per-symbol monotonic +1; **not** the matching updateId).

    * `pu` = the previous frame's `u` (delta frames only; snapshot has no `pu`).

    * `b`/`a` levels `[price, quantity]`: `quantity == "0"` removes the level, otherwise upsert.
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
                    "ch": "depth@btc_usdt",    // channel
                    "type": "delta",           // snapshot | delta
                    "u": 1025,                 // push local sequence (+1)
                    "pu": 1024,                // previous frame u (delta only)
                    "b": [                     // bids [0]price [1]quantity ("0" = remove)
                        [
                            "32000",
                            "0"
                        ]
                    ],
                    "a": [                     // asks [0]price [1]quantity
                        [
                            "34001",
                            "1.05"
                        ]
                    ],
                    "ts": 1657699200010        // time (ms)
                }
        title: delta
        language: json
---

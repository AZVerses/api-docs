---
title: Orderbook 维护
position_number: 7
split: -------------------------------------
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
        **如何正确在本地维护一个orderbook副本**


        全深度频道 `depth@<symbol>` 采用订阅即下发快照 + 增量的范式（类 Bybit）。不再 REST 拉快照、不再对齐撮合 updateId。


        1.订阅 `depth@btc_usdt`。


        2.第一帧为快照（`type` = `snapshot`）：整本替换本地簿，并记录 `lastU = u`。


        3.之后每个增量（`type` = `delta`）：若 `pu == lastU`，逐档应用并令 `lastU = u`；否则丢弃本地簿并重订阅（或等待服务端主动重发快照）。


        4.每档为该价位挂单量绝对值；量为 `"0"` 表示删除该价位，否则 upsert。


        5.服务端在重启 / 客户端落后时主动重发快照，故序列断裂在下一个快照自愈。


        注意：此处 `u` 为 push 本地序列（per-symbol 单调 +1），与定档深度频道（`depth20|depth50|depth100@<symbol>`，其 `u` 为撮合 updateId）不同源，切勿混用。

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

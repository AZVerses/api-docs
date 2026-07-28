---
title: Orderbook manage
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
        **How to manage a local order book correctly**


        The full-depth channel `depth@<symbol>` follows a subscribe-time snapshot + delta model (Bybit style). You no longer pull a REST snapshot or align on the matching-engine updateId.


        1.Subscribe to `depth@btc_usdt`.


        2.The first frame is a snapshot (`type` = `snapshot`): replace your whole local book and record `lastU = u`.


        3.For each following delta (`type` = `delta`): if `pu == lastU`, apply the levels one by one and set `lastU = u`; otherwise discard the local book and re-subscribe (or wait for the server to actively re-push a snapshot).


        4.Each level is the absolute quantity for a price level; a level whose quantity is `"0"` is removed, otherwise upsert.


        5.The server re-pushes a snapshot on restart / when the client falls behind, so a broken sequence self-heals on the next snapshot.


        Note: `u` here is the push local sequence (per-symbol monotonic +1), which is a different source from the fixed-level depth channels (`depth20|depth50|depth100@<symbol>`) where `u` is the matching updateId. Do not mix the two.

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

---
title: General WSS information
position_number: 1
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
  
    #### **Base Address**


    **production environment: wss://f-ws.azverse.xyz/futures/public**
    {: .info}

    **sandbox environment: wss://f-ws.az-qa.xyz/futures/public**
    {: .info}


    ---


    #### **Protocol**


    * Subscribe with `{"method":"subscribe","params":["ticker@btc_usdt"],"id":<n>}`; ack is `{"id":<n>,"result":"ok"}` or `{"id":<n>,"error":"<reason>"}`.

    * Most channels are flat frames carrying `ch` (e.g. `"ch":"ticker@btc_usdt"`).

    * Heartbeat is JSON `{"method":"ping"}` -> `{"pong":<ts>}`; idle timeout disconnects.

    * Symbol in channels uses lowercase underscore, e.g. `btc_usdt`.

    * Full depth uses subscribe-time snapshot + delta (the server re-pushes a snapshot on restart / when the client falls behind); no REST snapshot pull is needed.

    * Futures extras: the `ticker` frame carries `ix`/`mx` (index / mark price); a dedicated `fundrate@<symbol>` channel is available; and `index_price@<symbol>` / `mark_price@<symbol>` are separate flat-`ch` channels pushed strictly once per second.
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

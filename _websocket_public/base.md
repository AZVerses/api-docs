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


    **production environment: wss://s-ws.azverse.xyz/spot/public**
    {: .info}

    **sandbox environment: wss://s-ws.az-qa2.xyz/spot/public**
    {: .info}


    ---


    #### **Protocol**


    * Subscribe with `{"method":"subscribe","params":["ticker@btc_usdt"],"id":<n>}`; ack is `{"id":<n>,"result":"ok"}` or `{"id":<n>,"error":"<reason>"}`.

    * Most channels are flat frames carrying `ch` (e.g. `"ch":"ticker@btc_usdt"`).

    * Heartbeat is JSON `{"method":"ping"}` -> `{"pong":<ts>}`; idle timeout disconnects.

    * Symbol in channels uses lowercase underscore, e.g. `btc_usdt`.

    * Full depth uses subscribe-time snapshot + delta (the server re-pushes a snapshot on restart / when the client falls behind); no REST snapshot pull is needed.
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

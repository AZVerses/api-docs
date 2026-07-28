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

    **production environment: wss://s-ws.azverse.xyz/ws/account/spot**
    {: .info}

    **sandbox environment: wss://s-ws.az-qa2.xyz/ws/account/spot**
    {: .info}


    ---


    #### **Protocol**


    * The token is carried **on the handshake** (there is no LOGIN message any more). Fetch it from `/az/spot/ws-token` and pass it as `?token=<accessToken>` (or `?zToken=`) in the query string, or as a `token` / `zToken` cookie, or as an `Authorization: Bearer <accessToken>` header.

    * Authentication is **fail-closed**: a missing / invalid / expired token, or a wrong path, is rejected with HTTP `401` and the connection is closed.

    * The account is taken from the token — subscription channel names carry **no** `@accountId` suffix.

    * Subscribe with `{"method":"subscribe","params":["balance","order"],"id":<n>}`; ack is `{"id":<n>,"code":200,"msg":"success"}` on success or `{"id":<n>,"code":400,"msg":"<reason>"}` on failure.

    * Push frames are flat and carry `ch`: `{"ch":"balance","data":{...},"ts":<ts>}`.

    * Channels: `balance`, `order`, `trade`, `entrust`, `pred_position` (spot-only). Subscribing to a channel outside the spot domain returns `400`.

    * Heartbeat is text `ping` -> `pong`. The connection is disconnected after 60s of read idle.


    #### **Request Headers**

    The request header of the compression extension protocol must be added.

    <font color="#aa5500">Sec-Websocket-Extensions:permessage-deflate</font>  
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

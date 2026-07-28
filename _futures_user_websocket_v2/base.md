---
title: General WSS information
position_number: 1
type:
description:
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    #### **Base Address**

    **production environment: wss://f-ws.azverse.xyz/ws/account/futures**
    {: .info}

    **sandbox environment: wss://f-ws.az-qa.xyz/ws/account/futures**
    {: .info}


    ---


    #### **Request Headers**

    The request header of the compression extension protocol must be added.

    <font color="#aa5500">Sec-Websocket-Extensions:permessage-deflate</font>


    ---


    #### **Protocol**

    * **Authentication is at handshake time (fail-closed).** Carry a valid, unexpired login token on the WebSocket upgrade request in any one of: query string (`?token=<token>` or `?zToken=<token>`), cookie (`token` / `zToken`), or `Authorization: Bearer <token>` header. If the token is missing / invalid / expired, the server rejects the handshake with **HTTP 401** and closes the connection (there is no in-band error frame).

    * Subscribe with plain channel names (no `@listenKey` suffix): `{"method":"SUBSCRIBE","params":["order"],"id":"test1"}`; the ack is `{"id":"test1","code":200,"msg":"success"}`.

    * Push frames are flat and carry a `ch` field (the channel name), the payload `data`, and a server millisecond timestamp `ts`: `{"ch":"order","data":{...},"ts":1731231231000}`.

    * Heartbeat is the plain text `ping` -> `pong`; the connection is disconnected after 60s reader idle.

    * User-related data is pushed after a successful subscription.
left_code_blocks:
-
    code_block:
    title:
    language:
right_code_blocks:
-
    code_block:
    title:
    language:
---

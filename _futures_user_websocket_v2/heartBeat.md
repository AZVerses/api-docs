---
title: Heartbeat & limits
position_number: 5
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
    **Heartbeat**

    The client sends the plain text `ping` (a text frame, not JSON) periodically (recommended every <= 30s), and the server replies with the plain text `pong`. The connection is disconnected after **60s** of reader idle (no inbound frame).

    ---

    **Connection & rate limits**

    * The number of concurrent connections is capped per account and per client IP; exceeding the cap rejects the handshake with **HTTP 429**.
    * Inbound messages are rate limited per connection (`ping` counts too). When the limit is exceeded the server replies in-band with `{"id":null,"code":429,"msg":"rate_limited"}`.
    * The number of subscriptions per connection may also be capped; over-subscribing returns a `code:400` ack.
left_code_blocks:
    -
        code_block: 'ping'
        title: ping
        language: text
right_code_blocks:
    -
        code_block: 'pong'
        title: pong
        language: text
---

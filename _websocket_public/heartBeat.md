---
title: Heartbeat
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
content_markdown: The client sends `{"method":"ping"}` (JSON) periodically (recommended every <= 30s), and the server replies `{"pong":<ts>}` where `ts` is the server epoch millisecond timestamp. The connection is disconnected on idle timeout.
left_code_blocks:
    -
        code_block: '{"method":"ping"}'
        title: ping
        language: javascript
right_code_blocks:
    -
        code_block: '{"pong": 1661856036925}'
        title: pong
        language: json
---

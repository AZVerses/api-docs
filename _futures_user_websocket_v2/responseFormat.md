---
title: Response message format
position_number: 3
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
    The subscribe / unsubscribe ack is `{"id":"{id}","code":200,"msg":"success"}` on success.

    On failure the `code` is:

    * `400` — bad request (invalid param, unknown method, unknown channel, or channel not allowed for this domain);
    * `429` — rate limited (inbound message rate or connection limit exceeded).

    An invalid / expired token is **not** reported in-band: the handshake is rejected with HTTP 401 and the connection is closed before any WebSocket frame is exchanged.
left_code_blocks:
    -
        code_block: |-
            {
                "id": "{id}",   //call back ID
                "code": 200,    //result 200=success;400=bad request;429=rate limited
                "msg": ""
            }
        title: format
        language: javascript
right_code_blocks:
    -
        code_block: '{"id":"123", "code": 200, "msg": "success"}'
        title: Response-success
        language: json
    -
        code_block: '{"id":"123", "code": 400, "msg": "unknown channel: xxx"}'
        title: Response-error
        language: json
---

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
    The subscribe / unsubscribe ack is `{"id":<n>,"result":"ok"}` on success, or `{"id":<n>,"error":"<reason>"}` on failure (e.g. the server rejects the subscription while warm-up is not ready).
left_code_blocks:
    -
        code_block: |-
            {
                "id": 1,          //call back ID
                "result": "ok"
            }
        title: format
        language: javascript
right_code_blocks:
    -
        code_block: '{"id": 1, "result": "ok"}'
        title: Response-success
        language: json
    -
        code_block: '{"id": 1, "error": "invalid channel"}'
        title: Response-error
        language: json
---

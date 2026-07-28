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
    The subscribe / unsubscribe ack keeps the `{id,code,msg}` shape, but `code` is now `200` on success and `400` on failure (e.g. an unknown method, a bad param, or a channel outside the spot domain).
left_code_blocks:
    -
        code_block: |-
            {
                "id": "{id}",  //call back ID
                "code": 200,   //result 200=success;400=fail
                "msg": "success"
            }
        title: format
        language: javascript
right_code_blocks:
    -
        code_block: '{"id": "1", "code": 200, "msg": "success"}'
        title: Response-success
        language: json
    -
        code_block: '{"id": "1", "code": 400, "msg": "invalid param"}'
        title: Response-error
        language: json
---

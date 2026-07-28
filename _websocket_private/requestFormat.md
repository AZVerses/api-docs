---
title: Request message format
position_number: 2
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
    **param format**

    Each entry in `params` is a plain channel name (no `@accountId` suffix — the account is taken from the handshake token).

    Channels: `balance` , `order` , `trade` , `entrust` , `pred_position` .
left_code_blocks:
    -
        code_block: |-
                {
                    "method": "subscribe", 
                    "params": [
                        "balance",
                        "order"
                    ], 
                    "id": "{id}"
                }
        title: subscribe
        language: javascript
    -
        code_block: |-
            {
                "method": "unsubscribe", 
                "params": [
                    "balance",
                    "order"
                ], 
                "id": "{id}"
            }
        title: unsubscribe
        language: javascript
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

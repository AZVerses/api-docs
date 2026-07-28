---
title: Subscription parameters
position_number: 6
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
    **format**

    A plain channel name, one of:

    `order` , `trade` , `balance` , `position` , `notify` , `entrust` , `profit` , `track_entrust` , `user_profile` , `plan_reverse_entrust` .

    There is no `@listenKey` (or any other) suffix — the account is bound from the login token at handshake time.
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

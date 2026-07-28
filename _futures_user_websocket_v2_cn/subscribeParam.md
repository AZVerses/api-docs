---
title: 订阅参数
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
    **结构**

    纯频道名，取值之一：

    `order` , `trade` , `balance` , `position` , `notify` , `entrust` , `profit` , `track_entrust` , `user_profile` , `plan_reverse_entrust` 。

    无 `@listenKey`（或任何其它）后缀 —— 账号在握手阶段由登录 token 绑定。
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

---
title: 请求报文格式
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
    **param结构**

    `params` 中每一项为纯频道名（不带 `@accountId` 后缀——账户由握手 token 解析得到）。

    频道：`balance`、`order`、`trade`、`entrust`、`pred_position`。
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
        title: 订阅
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
        title: 取消订阅
        language: javascript
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---

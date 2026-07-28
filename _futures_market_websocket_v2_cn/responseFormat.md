---
title: 响应报文格式
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
    订阅 / 取消订阅应答：成功 `{"id":<n>,"result":"ok"}`，失败 `{"id":<n>,"error":"<reason>"}`（如服务端 warm-up 未就绪拒绝订阅）。
left_code_blocks:
    -
        code_block: |-
            {
                "id": 1,          //请求回调ID
                "result": "ok"
            }
        title: 响应报文格式
        language: javascript
right_code_blocks:
    -
        code_block: '{"id": 1, "result": "ok"}'
        title: Response-成功
        language: json
    -
        code_block: '{"id": 1, "error": "invalid channel"}'
        title: Response-失败
        language: json
---

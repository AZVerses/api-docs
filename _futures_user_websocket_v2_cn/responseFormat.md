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
    订阅 / 取消订阅的应答成功时为 `{"id":"{id}","code":200,"msg":"success"}`。

    失败时 `code` 为：

    * `400` —— 请求错误（参数非法、未知 method、未知频道，或该频道不允许在当前域订阅）；
    * `429` —— 被限流（入站消息速率或连接数超限）。

    token 无效 / 过期**不会**在 in-band 返回：握手直接被 HTTP 401 拒绝并关闭连接，此时尚未交换任何 WebSocket 帧。
left_code_blocks:
    -
        code_block: |-
            {
                "id": "{id}",   //请求回调ID
                "code": 200,    //结果 200=成功;400=请求错误;429=被限流
                "msg": ""
            }
        title: 响应报文格式
        language: javascript
right_code_blocks:
    -
        code_block: '{"id":"123", "code": 200, "msg": "success"}'
        title: Response-成功
        language: json
    -
        code_block: '{"id":"123", "code": 400, "msg": "unknown channel: xxx"}'
        title: Response-错误
        language: json
---

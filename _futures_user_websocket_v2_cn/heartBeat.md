---
title: 心跳与限制
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
content_markdown: |-
    **心跳**

    客户端周期性发送纯文本 `ping`（文本帧，非 JSON，建议 <= 30s 一次），服务端回复纯文本 `pong`。连接在**空闲 60s**（无入站帧）后被断开。

    ---

    **连接与限流**

    * 并发连接数按账号与按客户端 IP 分别设上限；超限时握手被 **HTTP 429** 拒绝。
    * 每连接的入站消息按速率限流（`ping` 也计入）。超限时服务端 in-band 返回 `{"id":null,"code":429,"msg":"rate_limited"}`。
    * 每连接的订阅数也可能设上限；超订阅返回 `code:400` 应答。
left_code_blocks:
    -
        code_block: 'ping'
        title: ping
        language: text
right_code_blocks:
    -
        code_block: 'pong'
        title: pong
        language: text
---

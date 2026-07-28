---
title: 心跳
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
content_markdown: 客户端定期发送 JSON `{"method":"ping"}`（建议每 <= 30s 一次），服务端回复 `{"pong":<ts>}`，其中 `ts` 为服务端毫秒时间戳。空闲超时服务端主动断开链接。
left_code_blocks:
    -
        code_block: '{"method":"ping"}'
        title: ping
        language: javascript
right_code_blocks:
    -
        code_block: '{"pong": 1661856036925}'
        title: pong
        language: json
---

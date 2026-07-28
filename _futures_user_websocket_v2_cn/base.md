---
title: 基本信息
position_number: 1
type:
description:
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    #### **基地址**

    **生产环境: wss://f-ws.azverse.xyz/ws/account/futures**
    {: .info}

    **测试环境: wss://f-ws.az-qa.xyz/ws/account/futures**
    {: .info}


    ---


    #### **Request Headers**

    请求头必须添加压缩扩展协议。

    <font color="#aa5500">Sec-Websocket-Extensions:permessage-deflate</font>


    ---


    #### **协议**

    * **鉴权在握手阶段完成（fail-closed）。** 在 WebSocket 升级请求上携带有效且未过期的登录 token，三选一：query（`?token=<token>` 或 `?zToken=<token>`）、cookie（`token` / `zToken`）、或 `Authorization: Bearer <token>` 头。若 token 缺失 / 无效 / 过期，服务端以 **HTTP 401** 拒绝握手并关闭连接（不返回任何 in-band 错误帧）。

    * 用纯频道名订阅（无 `@listenKey` 后缀）：`{"method":"SUBSCRIBE","params":["order"],"id":"test1"}`；应答为 `{"id":"test1","code":200,"msg":"success"}`。

    * 推送帧为扁平结构，携带 `ch`（频道名）、`data`（数据）与服务端毫秒时间戳 `ts`：`{"ch":"order","data":{...},"ts":1731231231000}`。

    * 心跳为纯文本 `ping` -> `pong`；空闲 60s（无入站帧）后断开连接。

    * 订阅成功后会推送用户相关数据。
left_code_blocks:
-
    code_block:
    title:
    language:
right_code_blocks:
-
    code_block:
    title:
    language:
---

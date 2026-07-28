---
title: 基本信息
position_number: 1
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
    #### **基地址**

    **生产环境: wss://s-ws.azverse.xyz/ws/account/spot**
    {: .info}

    **测试环境: wss://s-ws.az-qa.xyz/ws/account/spot**
    {: .info}


    ---


    #### **协议（700 accounts-push 重构）**


    这是重构后的私有账户 WebSocket 协议。鉴权、订阅、推送、应答均与旧版不同，字段均为短键。


    * token 在**握手时携带**（不再有 LOGIN 报文）。从 `/az/spot/ws-token` 获取后，通过查询串 `?token=<accessToken>`（或 `?zToken=`）、或 `token` / `zToken` cookie、或 `Authorization: Bearer <accessToken>` 请求头传入。

    * 鉴权为 **fail-closed**：token 缺失/无效/过期，或路径错误，直接返回 HTTP `401` 并关闭连接。

    * 账户由 token 解析得到——订阅频道名**不带** `@accountId` 后缀。

    * 订阅：`{"method":"subscribe","params":["balance","order"],"id":<n>}`；应答成功为 `{"id":<n>,"code":200,"msg":"success"}`，失败为 `{"id":<n>,"code":400,"msg":"<原因>"}`。

    * 推送帧为扁平结构，带 `ch`：`{"ch":"balance","data":{...},"ts":<ts>}`。

    * 频道：`balance`、`order`、`trade`、`entrust`、`pred_position`（现货专有）。订阅现货域外的频道返回 `400`。

    * 心跳为文本 `ping` -> `pong`。连接在读空闲 60s 后断开。


    #### **Request Headers**

    请求头必须添加压缩扩展协议。

    <font color="#aa5500">Sec-Websocket-Extensions:permessage-deflate</font>  
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

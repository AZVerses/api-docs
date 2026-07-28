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


    **生产环境: wss://f-ws.azverse.xyz/futures/public**
    {: .info}

    **测试环境: wss://f-ws.az-qa.xyz/futures/public**
    {: .info}


    ---


    #### **协议**


    * 订阅：`{"method":"subscribe","params":["ticker@btc_usdt"],"id":<n>}`；应答 `{"id":<n>,"result":"ok"}` 或 `{"id":<n>,"error":"<reason>"}`。

    * 多数频道为扁平帧，带 `ch`（如 `"ch":"ticker@btc_usdt"`）。

    * 心跳为 JSON `{"method":"ping"}` -> `{"pong":<ts>}`；空闲超时断连。

    * 频道内 symbol 用小写下划线，如 `btc_usdt`。

    * 全深度采用订阅即下发快照 + 增量（服务端在重启 / 客户端落后时主动重发快照）；无需 REST 拉快照。

    * 合约专属：`ticker` 帧带 `ix`/`mx`（指数 / 标记价）；提供独立 `fundrate@<symbol>` 频道；`index_price@<symbol>` / `mark_price@<symbol>` 为独立的扁平 `ch` 频道，严格每秒下发。
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

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

    **生产环境: wss://s-ws.azverse.xyz/private**
    {: .info}

    **测试环境: wss://s-ws.az-qa.xyz/private**
    {: .info}


    ---

    #### **Request Parameter**
    <font color="#aa5500">?token={accessToken}</font> 
    accessToken 从 /az/spot/ws-token 接口中获取

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

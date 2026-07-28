---
title: 用户业务系统间划转
position_number: 1
type: post
description: /az/spot/balance/transfer
parameters:
    -
        name: bizId
        type: string
        mandatory: true
        default:
        description: 唯一id 用作重复请求幂等。仅允许字母、数字、'-' 和 '_'（正则 ^[A-Za-z0-9-_]+$）
        ranges: 最大长度为128
    -
        name: from
        type: enum
        mandatory: true
        default:
        description: 划出业务账户。from 与 to 不能相同（FUND_015），取值越界报 FUND_021
        ranges: SPOT / FUTURES_U
    -
        name: to
        type: enum
        mandatory: true
        default:
        description: 划入业务账户。from 与 to 不能相同（FUND_015），取值越界报 FUND_021
        ranges: SPOT / FUTURES_U
    -
        name: currency
        type: string
        mandatory: true
        default:
        description: 币种名称必须全部小写（usdt，btc）。币种不存在报 FUND_017
        ranges:
    -
        name: amount
        type: bigDecimal
        mandatory: true
        default:
        description: 划转的数量。必须为正数；末尾零会被去除，精度受币种 maxPrecision 约束（下限 10）
        ranges:

content_markdown: >-


left_code_blocks:
    -
        code_block: |-
            public String transferPost(){


            }
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [],
                  "result": 123456  //返回的划转唯一id 建议存储用来对账
                }
        title: Response
        language: json
---

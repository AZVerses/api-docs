---
title: 订单成交
position_number: 8
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
    param

    语法: trade

    示例: trade
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "trade",
                "data": {
                    "s": "btc_usdt",           //symbol
                    "i": 6316559590087222000,  //成交id
                    "t": 1655992403617,        //时间
                    "oi": 6616559590087222666, //订单id
                    "p": "43000",              //价格
                    "q": "0.21",               //数量
                    "v": "9030",               //金额
                    "b": true,                 //是否是buyerMaker
                    "tm": 1,                   //1-taker 2-maker
                    "rfq": false,              //是否为 RFQ 成交
                    "ouid": 6216559590087220004 //对手方 userId（仅预测市场 maker 可见）
                },
                "ts": 1655992403617
            }
        title: 推送
        language: json
---

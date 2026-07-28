---
title: 单笔撤单
position_number: 3
type: delete
split: -------------------------------------
description: /az/spot/order/{orderId}
parameters:
    -
        name: orderId
        type: number
        mandatory: true
        default:
        description: 订单ID
        ranges:
content_markdown: >-

left_code_blocks:
    -
        code_block: |-
            public String orderDel(){


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
                  "ma": [
                    {}
                  ],
                  "result": {
                    "orderId": "6216559590087220004",       //订单ID
                    "cancelId": "6216559590087220005",      //撤单ID
                    "clientCancelId": "16559590087220001"   //客户端撤单ID
                  }
                }
        title: Response
        language: json
---

---
title: 委托撤单
position_number: 15
type: delete
split: -------------------------------------
description: /az/spot/entrust-order/{entrustOrderId}
parameters:
    -
        name: entrustOrderId
        type: number
        mandatory: true
        default:
        description: 委托订单ID
        ranges:
content_markdown: >-

left_code_blocks:
    -
        code_block: |-
            public String entrustOrderDel(){


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
                    "orderId": "6216559590087220004",       //委托订单ID
                    "cancelId": "6216559590087220005",      //撤单ID
                    "clientCancelId": "16559590087220001"   //客户端撤单ID
                  }
                }
        title: Response
        language: json
---

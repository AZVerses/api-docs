---
title: builder用户列表查询
position_number: 13
type: get
description: /az/api/stats/v1/builder/user-list
parameters:
    -
        name: lastId
        type: number
        mandatory: false
        default:
        description: 分页查询，起始id
        ranges:
    -
        name: pageSize
        type: number
        mandatory: false
        default: '10'
        description: 每页数量，最大 100
        ranges:
content_markdown: >-
    #### **限流规则**

    10/s/apikey
left_code_blocks:
    -
        code_block:
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
            "code": 200,
            "msg": "Success.",
            "msgInfo": {
                "template": "Success.",
                "args": null,
                "code": null
            },
            "data": {
                "items": [{
                            "address": "0x17bdacf05b156786d28bc3876cb1d3adef7a5486",
                            "totalBalance": "9994.8559",
                            "perpetualBalance": "9994.8559",
                            "spotBalance": "0",
                            "position": "26.4339"
                        }],
                "nextId": "8878261469475",
                "hasMore": true
                }
            }
        title: Response
        language: json
---

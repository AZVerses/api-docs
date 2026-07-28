---
title: 用户配置
position_number: 15
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
  subscribe:
  ```js
    {
       "method": "SUBSCRIBE/UNSUBSCRIBE",
       "params": [
           "user_profile"
        ],
       "id": "{id}"
    }
  ```

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "user_profile",
                "data": {
                        "leverageMode": 1,               // 杠杆模式
                        "positionTypeAllSymbol": true,   // 仓位类型是否应用于所有交易对
                        "positionType": "ISOLATED",      // 仓位类型:CROSSED;ISOLATED（未设置时为null）
                        "updateTime": 1731231231000      // 更新时间(ms)
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

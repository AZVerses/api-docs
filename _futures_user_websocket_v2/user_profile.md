---
title: User profile
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
                        "leverageMode": 1,               // Leverage mode
                        "positionTypeAllSymbol": true,   // Whether the position type applies to all symbols
                        "positionType": "ISOLATED",      // Position type:CROSSED;ISOLATED (null when unset)
                        "updateTime": 1731231231000      // Update time (ms)
                   },
                "ts": 1731231231000
            }
        title: Response
        language: json
---

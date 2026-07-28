---
title: 响应报⽂格式
position_number: 3
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
    订阅/取消订阅应答保持 `{id,code,msg}` 结构，但 `code` 现为 `200`=成功、`400`=失败（如未知 method、参数错误、或订阅现货域外的频道）。
left_code_blocks:
    -
        code_block: |-
                {
                    "id": "{id}",   //请求回调ID
                    "code": 200,    //结果 200=成功;400=失败
                    "msg": "success"
                }
        title: 格式
        language: javascript
right_code_blocks:
    -
        code_block: '{"id": "1", "code": 200, "msg": "success"}'
        title: Response-success
        language: json
    -
        code_block: '{"id": "1", "code": 400, "msg": "invalid param"}'
        title: Response-error
        language: json
---

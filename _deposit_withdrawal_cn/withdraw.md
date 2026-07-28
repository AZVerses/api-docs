---
title: 提现
position_number: 4
type: post
description: /az/spot/withdraw
parameters:
    -
        name: 'fromAccount'
        type: string
        mandatory: false
        default: SPOT
        description: >-
               提现账户类型，现货或者是合约
        ranges: SPOT; FUTURES_U
    -
        name: 'currency'
        type: string
        mandatory: true
        default:
        description: >- 
                币种名称，可从'获取AZ可充提的币种'接口中获取
        ranges:
    -
        name: 'chain'
        type: string
        mandatory: true
        default:
        description: >-
                转账网络名称，可从'获取AZ可充提的币种'接口中获取。链上提现必填。
        ranges:
    -
        name: 'clientOrderId'
        type: string
        mandatory: false
        default:
        description: >-
                自定义客户端ID，正则：^[a-zA-Z0-9_]{4,32}$
        ranges:
    -
        name: 'amount'
        type: number
        mandatory: true
        default:
        description: >-
                提现金额，包含手续费部分
        ranges: 
    -
        name: 'address'
        type: string
        mandatory: true
        default:
        description: >-
                提现地址。必填——目前仅支持链上提现，内部转账暂不支持。
        ranges: 
    -
        name: 'memo'
        type: string
        mandatory: false
        default:
        description: >-
                memo，对于EOS类似的需要memo的链必传
        ranges:
    -
        name: 'toAccountId'
        type: number
        mandatory: false
        default:
        description: >-
          收款用户ID。暂不支持——内部转账当前已禁用，该参数会被忽略，仅支持链上提现。
        ranges:
content_markdown: |-
                注意：参数以json形式放在body中

                注意：目前仅支持链上提现，内部转账（toAccountId）暂不支持；未携带链上 `address` 的请求会被拒绝并返回 "Internal transfer is not supported."
                #### **限流规则**

                1/s/apikey
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
                    "currency":"zb",
                    "chain":"Ethereum",
                    "amount":1000,
                    "address":"0xfa3abfa50eb2006f5be7831658b17aca240d8526",
                    "memo":""
                }
        title: Request
        language: json
    -
        code_block: |-
                {
                    "rc": 0,
                    "mc": "SUCCESS",
                    "ma": [],
                    "result": {      
                        "id": 100    //Long  提现记录id，用于后期查询提现历史记录
                    }
                }
        title: Response
        language: json    
---

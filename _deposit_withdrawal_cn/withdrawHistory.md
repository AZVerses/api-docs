---
title: 提现历史
position_number: 6
type: get
description: /az/spot/withdraw/history
parameters:
    -
        name: 'currency'
        type: string
        mandatory: false
        default:
        description: >- 
                币种名称，可从'获取AZ可充提的币种'接口中获取
        ranges:
    -
        name: 'chain'
        type: string
        mandatory: false
        default:
        description: >-
                转账网络名称，可从'获取AZ可充提的币种'接口中获取
        ranges:
    -
        name: 'status'
        type: string
        mandatory: false
        default:
        description: >-
                提现记录的<a href="#depositWithdrawStatusCn">状态</a>，字符串类型（含义见公共模块-充值/提现记录状态码及含义）
        ranges: SUBMIT、REVIEW、AUDITED、AUDITED_AGAIN、PENDING、SUCCESS、FAIL、CANCEL
    -
        name: 'fromId'
        type: Long
        mandatory: false
        default:
        description: >-
                上次开始分页的Id，即记录的主键id
        ranges: 
    -
        name: 'direction'
        type: String
        mandatory: false
        default: NEXT
        description: >-
                分页方向
        ranges: NEXT：下一页，PREV：上一页
    -
        name: 'limit'
        type: int
        mandatory: false
        default: 10
        description: >-
                每页记录数，最大不超过200
        ranges: 1<=limit<=200
    -
        name: 'startTime'
        type: Long
        mandatory: false
        default: 
        description: >-
                查询范围开始边界，毫秒级时间戳。startTime 和 endTime 必须成对传入。
        ranges: 
    -
        name: 'endTime'
        type: Long
        mandatory: false
        default: 
        description: >-
                查询范围结束边界，毫秒级时间戳。startTime 和 endTime 必须成对传入。
        ranges: 

content_markdown: |-
                #### **时间范围规则**

                - `startTime` 和 `endTime` 必须成对传入，只传其中一个会报错。
                - 两者都不传时，默认查询最近 3 个月。
                - `startTime` 到 `endTime` 的跨度不能超过 6 个月。
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
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                        "hasPrev": true,                       //是否有上一页
                        "hasNext": true,                       //是否有下一页
                        "items": [
                            {
                                "id": 763111,                  //提现记录id
                                "clientOrderId": "10",         //客户端ID，字符串类型
                                "type": "CHAIN_TRANSFER",      //提现类型，字符串枚举名：CHAIN_TRANSFER-区块链提现，INTERNAL_TRANSFER-内部提现，CMS_TRANSFER-管理后台人工入账
                                "currency": "usdt",            //币种名称
                                "chain": "Ethereum",           //提现网络
                                "address": "0xfa3abfa50eb2",   //提现目标地址
                                "memo": "",
                                "needSwap": false,             //是否需要 USDT/USDC 互换
                                "fromAccount": "SPOT",         //资金来源账户，例如 SPOT、FUTURES
                                "swapCurrency": null,          //互换后币种（无互换时为 null）
                                "swapAmount": null,            //互换后数量，字符串类型（无互换时为 null）
                                "swapPrice": null,             //互换价格，字符串类型（无互换时为 null）
                                "status": "REVIEW",            //状态，含义见公共模块-充值/提现记录状态码及含义
                                "amount": "30",                //提现金额，字符串类型
                                "fee": "0",                    //提现手续费，字符串类型
                                "confirmations": 0,            //区块确认数
                                "transactionId": "",           //交易哈希
                                "createdTime": 1667763470000                                
                            },
                            {
                                "id": 763107,
                                "clientOrderId": "10", 
                                "type": "CHAIN_TRANSFER",  
                                "currency": "usdt",
                                "chain": "Tron",
                                "address": "TYnJJwaJKkqVvE2zEfUvFbHgKxVBY5zGq9",
                                "memo": "",
                                "needSwap": false,
                                "fromAccount": "SPOT",
                                "swapCurrency": null,
                                "swapAmount": null,
                                "swapPrice": null,
                                "status": "REVIEW",
                                "amount": "50",
                                "fee": "1",
                                "confirmations": 0,
                                "transactionId": "",
                                "createdTime": 1667428286000
                            }
                        ]
                  }
                }
        title: Response
        language: json
---


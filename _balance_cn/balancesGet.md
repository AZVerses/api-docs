---
title: 获取币种资产列表
position_number: 3
type: get
split: -------------------------------------
description: /az/spot/balances
parameters:
    -
        name: currencies
        type: string
        mandatory: false
        default:
        description: '币种列表,逗号分隔，eg:  usdt,btc'
        ranges:
    -
        name: queryAccountId
        type: long
        mandatory: false
        default:
        description: 查询账户id，不传递默认使用当前账户id。主账户不允许被查询
        ranges:
    -
        name: filterIsDisplayFalse
        type: boolean
        mandatory: false
        default: 'true'
        description: 是否过滤掉 isDisplay 为 false 的币种
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
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                    "totalUsdtAmount": "0",      //折算USDT总资产
                    "availableUsdtAmount": "0",  //折算USDT可用资产
                    "totalBtcAmount": "0",       //折算BTC总资产
                    "assets": [    //参数内容参考获取单个币种资产接口
                      {
                        "currency": "string",
                        "currencyId": 0,
                        "frozenAmount": "0",       //不可用(冻结+锁仓+跟单+委托+提现)
                        "freeze": "0",             //冻结
                        "lock": "0",               //锁仓
                        "trade": "0",              //委托
                        "withdraw": "0",           //提现
                        "availableAmount": "0",    //可用数量
                        "totalAmount": "0",        //总数量
                        "convertBtcAmount": "0",   //折算BTC数量
                        "convertUsdtAmount": "0",  //折算USDT数量
                        "convertAvailableUsdtAmount": "0"  //折算USDT可用数量
                      }
                    ]
                  }
                }
        title: Response
        language: json
---


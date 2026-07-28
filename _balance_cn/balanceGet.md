---
title: 获取单个币种资产
position_number: 2
type: get
description: /az/spot/balance
parameters:
    -
        name: currency
        type: string
        mandatory: true
        default:
        description: eg:usdt
        ranges:
content_markdown:
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
                    "currency": "usdt",        //币种
                    "currencyId": 0,           //币种ID
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
                }
        title: Response
        language: json
---


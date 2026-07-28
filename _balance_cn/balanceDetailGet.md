---
title: 获取现货+合约资产明细
position_number: 4
type: get
description: /az/spot/balance/detail
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    现货+合约资产明细聚合：汇总折算 + 现货逐币种明细 + 合约逐币种明细。
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
                    "summary": {
                      "totalValue": "0",           //总资产折算USDT
                      "spotBalance": "0",          //现货余额折算USDT
                      "perpsBalance": "0",         //合约余额折算USDT(含未实现盈亏)
                      "perpsWalletBalance": "0",   //合约钱包余额折算USDT
                      "perpsBotBalance": "0",      //合约策略机器人余额折算USDT
                      "vaultBalance": "0",         //vault余额折算USDT(含未实现盈亏)
                      "predictBalance": "0",       //预测市场未结算持仓估值折算USDT
                      "unrealizedPnl": "0",        //合约未实现盈亏(USDT)
                      "availableAmount": "0"       //可用余额(USDT)
                    },
                    "spotDetails": [
                      {
                        "currency": "usdt",
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
                    ],
                    "perpDetails": [
                      {
                        "accountId": 0,
                        "userId": 0,
                        "coin": "usdt",            //结算币种
                        "underlyingType": 1,       //合约类型(U本位/币本位)
                        "walletBalance": "0",      //钱包余额
                        "openOrderMarginFrozen": "0",  //挂单占用保证金
                        "isolatedMargin": "0",     //逐仓保证金
                        "amount": "0",             //可用数量
                        "totalAmount": "0",        //总数量
                        "profit": "0",             //已实现盈亏
                        "notProfit": "0"           //未实现盈亏
                      }
                    ]
                  }
                }
        title: Response
        language: json
---


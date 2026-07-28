---
title: 获取AZ可充提的币种
position_number: 1
type: get
description: /az/spot/public/wallet/support/currency
parameters:
    

content_markdown: >-
    #### **备注**

    currency  、chain 字段需要在后续充值/提现接口中使用
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
                  "result": [
                    {
                        "currency": "BTC",                       //币种
                        "supportChains": [
                            {
                                "chain": "Bitcoin",              //支持的转账网络
                                "depositEnabled": true,          //是否支持充值，true:支持，false:不支持
                                "withdrawEnabled": true,         //是否支持提现，true:支持，false:不支持
                                "contract": "contractaddress",   //合约地址
                                "depositMinAmount": 0.0001,      //最小充值数量
                                "depositFeeRate": 0,             //充值费率，恒为 0（充值不收费）
                                "depositConfirmations": 2,       //充值所需区块确认数
                                "withdrawMinAmount": 10,         //最小提现数量
                                "withdrawPrecision": 8,          //提币数量精度（小数位数）
                                "withdrawFeeAmount": 0.2,        //提现手续费
                                "withdrawFeeCurrency": "BTC",    //提现手续费币种名称
                                "withdrawFeeCurrencyId": 1       //提现手续费币种id
                            }
                        ]           
                    },
                    {
                        "currency": "ETH",                       //币种
                        "supportChains": [
                            {
                                "chain": "Ethereum",             //支持的转账网络
                                "depositEnabled": true,          //是否支持充值，true:支持，false:不支持
                                "withdrawEnabled": true,         //是否支持提现，true:支持，false:不支持
                                "contract": "contractaddress",   //合约地址
                                "depositMinAmount": 0.01,        //最小充值数量
                                "depositFeeRate": 0,             //充值费率，恒为 0（充值不收费）
                                "depositConfirmations": 12,      //充值所需区块确认数
                                "withdrawMinAmount": 10,         //最小提现数量
                                "withdrawPrecision": 8,          //提币数量精度（小数位数）
                                "withdrawFeeAmount": 0.2,        //提现手续费
                                "withdrawFeeCurrency": "ETH",    //提现手续费币种名称
                                "withdrawFeeCurrencyId": 2       //提现手续费币种id
                            }
                        ]
                    }
                  ]
                }
        title: Response
        language: json
---

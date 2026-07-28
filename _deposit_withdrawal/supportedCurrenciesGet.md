---
title: Get information of currencies (available for deposit and withdraw)
position_number: 1
type: get
description: /az/spot/public/wallet/support/currency
parameters:
    
        
content_markdown: >-
    #### **Remark**

    The currency and chain in the response need to be used in other deposit/withdrawal API
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
                        "currency": "BTC",                       //currency name
                        "supportChains": [
                            {
                                "chain": "Bitcoin",              //supported transfer network
                                "depositEnabled": true,          //deposit is supported or not
                                "withdrawEnabled": true,         //withdraw is supported or not
                                "contract": "contractaddress",   //contract address
                                "depositMinAmount": 0.0001,      //minimum deposit amount
                                "depositFeeRate": 0,             //deposit fee rate, always 0 (deposit is free of charge)
                                "depositConfirmations": 2,       //number of block confirmations required for deposit
                                "withdrawMinAmount": 10,         //minimum withdrawal amount
                                "withdrawPrecision": 8,          //withdrawal amount precision (decimal places)
                                "withdrawFeeAmount": 0.2,        //withdrawal fee
                                "withdrawFeeCurrency": "BTC",    //currency name of the withdrawal fee
                                "withdrawFeeCurrencyId": 1       //currency id of the withdrawal fee
                            }
                        ]           
                    },
                    {
                        "currency": "ETH",                       //currency name
                        "supportChains": [
                            {
                                "chain": "Ethereum",             //supported transfer network
                                "depositEnabled": true,          //deposit is supported or not
                                "withdrawEnabled": true,         //withdraw is supported or not
                                "contract": "contractaddress",   //contract address
                                "depositMinAmount": 0.01,        //minimum deposit amount
                                "depositFeeRate": 0,             //deposit fee rate, always 0 (deposit is free of charge)
                                "depositConfirmations": 12,      //number of block confirmations required for deposit
                                "withdrawMinAmount": 10,         //minimum withdrawal amount
                                "withdrawPrecision": 8,          //withdrawal amount precision (decimal places)
                                "withdrawFeeAmount": 0.2,        //withdrawal fee
                                "withdrawFeeCurrency": "ETH",    //currency name of the withdrawal fee
                                "withdrawFeeCurrencyId": 2       //currency id of the withdrawal fee
                            }
                        ]
                    }
                  ]
                }
        title: Response
        language: json
---

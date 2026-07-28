---
title: 获取币种信息
position_number: 1
type: get
description: /az/spot/public/currencies
parameters:
    -
        name: builder-code
        type: string
        mandatory: false
        default:
        description: '请求头。builder code，eg: azx'
        ranges:
    -
        name: client-lang
        type: string
        mandatory: false
        default: en
        description: '请求头。客户端语言，eg: en/cn'
        ranges:
    -
        name: version
        type: string
        mandatory: false
        default:
        description: 内容版本号(query)。当请求版本号与响应内容版本一致时，不返回清单，减少IO
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
                    "time": 1661856036925,   //时间戳(毫秒)
                    "version": "2e14d2cd5czcb2c2af2c1db65078d075",  //内容版本
                    "currencies": [
                      {
                          "id": 2,               //币种id
                          "currency": "btc",     //币种名称
                          "displayName": "BTC",  //币种展示名称
                          "displayNames": {      //i18n展示名，键=语言码，en恒在
                              "en": "BTC",
                              "cn": "BTC"
                          },
                          "type": "FT",          //币种类型: FT | NFT
                          "nominalValue": "1",   //面值
                          "fullName": "Bitcoin", //币种全称
                          "logo": "https://a.static-global.com/1/currency/btc.png",
                          "cmcLink": "https://coinmarketcap.com/currencies/bitcoin/",
                          "weight": 99999,
                          "isBlack": false,      //当前builder是否屏蔽该币种
                          "maxPrecision": 10,
                          "depositStatus": 0,    //充值状态(0关闭 1开放)
                          "withdrawStatus": 0,   //提现状态(0关闭 1开放)
                          "isDisplay": 1,        //是否显示(0否 1是)
                          "convertEnabled": 1,   //小额资产兑换开关[0=关;1=开]
                          "transferEnabled": 1,  //划转开关[0=关;1=开]
                          "isChainExist": 1,
                          "plates": [],
                          "isListing": 1,
                          "withdrawCloseReason": "CURRENCY_CLOSE_REASON_5",
                          "chainRelation": [
                              {
                                  "chainId": 715,
                                  "web3ChainId": 42161,  //web3 chain id
                                  "contract": "0x7130d2A12B9BCbFAe4f2634d864A1Ee1Ce3Ead9c"
                              },
                              {
                                  "chainId": 5,
                                  "web3ChainId": 1,
                                  "contract": "0x9BE89D2a4cd102D8Fecc6BF9dA793be995C22541"
                              }
                          ]
                      }
                    ]
                  }
                }
        title: Response
        language: json
---


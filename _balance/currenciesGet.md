---
title: Get currency information
position_number: 1
type: get
description: /az/spot/public/currencies
parameters:
    -
        name: builder-code
        type: string
        mandatory: false
        default:
        description: 'Request header. Builder code, eg: azx'
        ranges:
    -
        name: client-lang
        type: string
        mandatory: false
        default: en
        description: 'Request header. Client language, eg: en/cn'
        ranges:
    -
        name: version
        type: string
        mandatory: false
        default:
        description: Content version (query). When the request version matches the response content version, the currency list is not returned to reduce IO
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
                "time": 1661856036925,   //timestamp (ms)
                "version": "2e14d2cd5czcb2c2af2c1db65078d075",  //content version
                "currencies": [
                  {
                      "id": 2,               //currency id
                      "currency": "btc",     //currency name
                      "displayName": "BTC",  //currency display name
                      "displayNames": {      //i18n display names, keyed by language code, en always present
                          "en": "BTC",
                          "cn": "BTC"
                      },
                      "type": "FT",          //currency type: FT | NFT
                      "nominalValue": "1",   //nominal value
                      "fullName": "Bitcoin", //full name
                      "logo": "https://a.static-global.com/1/currency/btc.png",
                      "cmcLink": "https://coinmarketcap.com/currencies/bitcoin/",
                      "weight": 99999,
                      "isBlack": false,      //whether the current builder blocks this currency
                      "maxPrecision": 10,
                      "depositStatus": 0,    //Recharge status(0 close 1 open)
                      "withdrawStatus": 0,   //Withdrawal status(0 close 1 open)
                      "isDisplay": 1,        //whether to display(0 no 1 yes)
                      "convertEnabled": 1,   //Small asset exchange switch[0=close;1=open]
                      "transferEnabled": 1,  //swipe switch[0=close;1=open]
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


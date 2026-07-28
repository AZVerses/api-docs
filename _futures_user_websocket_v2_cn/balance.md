---
title: 余额变更
position_number: 7
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
  subscribe:
  ```js
    {
       "method": "SUBSCRIBE/UNSUBSCRIBE",
       "params": [
           "balance"
        ],
       "id": "{id}"
    }
  ```

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "ch": "balance",
                "data": {
                            "coin": "usdt",                        //币种
                            "underlyingType": 2,                   //1:币本位，2:U本位
                            "walletBalance": "9652.09217635",      //钱包余额
                            "openOrderMarginFrozen": "0.00000000", //逐仓订单冻结保证金
                            "isolatedMargin": "0",                 //逐仓保证金
                            "crossedMargin": "0",                  //全仓保证金（恒为0，见 virtualCrossMargin）
                            "availableBalance": "9613.51195739",   //可用余额
                            "virtualCrossMargin": "38.58021896",   //虚拟全仓保证金（仅 usdt，其它币种为0）
                            "virtualOpenOrderMarginFrozen": "0.00000000", //虚拟全仓订单冻结保证金（仅 usdt，其它币种为0）
                            "virtualCrossNotProfit": "0"           //虚拟全仓未实现盈亏
                   },
                "ts": 1762184243057
            }
        title: Response
        language: json
---

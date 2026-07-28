---
title: 仓位变更
position_number: 8
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
           "position"
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
                "ch": "position",
                "data": {
                            "accountId": 8654006125462,    //账号id
                            "accountType": 0,              //账号类型
                            "symbol": "btc_usdt",          //交易对
                            "contractType": "PERPETUAL",   //合约类型，PERPETUAL，DELIVERY
                            "positionType": "CROSSED",     //"ISOLATED", "CROSSED"
                            "positionSide": "LONG",        //仓位方向
                            "positionSize": "0.2",         //持仓数量（标的币）
                            "closeOrderSize": "0",         //平仓挂单数量（标的币）
                            "availableCloseSize": "0.2",   //可平数量（标的币）
                            "realizedProfit": "-113.4475", //已实现盈亏
                            "entryPrice": "107577.0",      //开仓均价
                            "openOrderSize": "0",          //开仓订单占用数量（标的币）
                            "isolatedMargin": "21.59097358", //逐仓保证金
                            "openOrderMarginFrozen": "0.00000000", //开仓订单占用保证金
                            "underlyingType": "U_BASED",    //COIN_BASED, U_BASED
                            "leverage": 10,                //杠杆倍数
                            "state": 1,                    //仓位状态
                            "closeProfit": "232.7172",     //平仓盈亏
                            "totalFee": "-133.1456",       //手续费
                            "totalFundFee": "-213.0191",   //资金费用
                            "markPrice": "106208.1",       //标记价格
                            "marginCoin": "usdt",          //保证金币种
                            "profitId": "556931318219666113",   //全仓止盈止损id（无则为null）
                            "triggerPriceType": "LATEST_PRICE", //全仓止盈止损触发价格类型
                            "triggerProfitPrice": "120000.0",   //全仓止盈触发价
                            "triggerStopPrice": "100000.0",     //全仓止损触发价
                            "profitFixedLatest": {              //最新的部分仓位止盈止损（无则为空对象 {}）
                                "profitId": "556931318219666114",
                                "triggerPriceType": "LATEST_PRICE",
                                "triggerProfitPrice": "121000.0",
                                "triggerStopPrice": "99000.0"
                            },
                            "profitFixedCount": 2,         //部分仓位止盈止损总数
                            "updatedTime": 1762184243057
                   },
                "ts": 1762184243057
            }
        title: Response
        language: json
---

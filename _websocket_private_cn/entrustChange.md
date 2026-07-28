---
title: 委托变动
position_number: 6
display: 0
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
    param

    语法: entrust

    示例: entrust
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "ch": "entrust",
                    "data": {
                        "t": 1656043204763,             // time 发⽣时间
                        "ct": 1656043204663,            // createTime 创建时间
                        "s": "btc_usdt",                // symbol 交易对
                        "sd": "BUY",                    // side 方向 BUY/SELL
                        "tp": "3",                      // type 类型 3=止盈止损(ENTRUST_PROFIT),4=跟踪委托(ENTRUST_TRACK)
                        "bt": "1",                      // bizType 业务类型 1=SPOT(现货)
                        "st": "1",                      // state 状态 1=新建(NEW),2=已触发(TRIGGERED),3=已过期(EXPIRED),4=已撤销(CANCELED)
                        "ast": "0",                     // 跟踪委托激活状态 0=未激活(INACTIVE),1=已激活(ACTIVE)
                        "qt": "2",                      // quantity 数量
                        "qty": "2",                     // quoteQty 金额（跟踪委托买入时输入）
                        "tgp": "30000",                 // triggerPrice 触发价格（止盈止损使用）
                        "p": "30000",                   // price 委托价格（止盈止损使用）
                        "cp": "31000",                  // 下止盈止损或跟踪委托时的价格
                        "acp": "32000",                 // activePrice 激活价格（跟踪委托使用）
                        "tr": "0.05",                   // turnRate 回调幅度（跟踪委托使用）
                        "pd": "100",                    // priceDiff 价距（跟踪委托使用）
                        "ep": "29000",                  // extremePrice 下单以来最高/最低价（跟踪委托使用）
                        "i": "6216559590087220004",     // orderId 订单号
                        "ci": "test123"                 // clientOrderId 客户端订单号
                    },
                    "ts": 1656043204763
                }
        title: 推送
        language: json
---

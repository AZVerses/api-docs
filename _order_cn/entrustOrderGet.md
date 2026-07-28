---
title: 委托单笔获取
position_number: 16
type: get
description: /az/spot/entrust-order/{entrustOrderId}
parameters:
    -
        name: entrustOrderId
        type: number
        mandatory: true
        default:
        description: 委托订单ID
        ranges:
content_markdown: >-

left_code_blocks:
    -
        code_block: |-
            public String entrustOrderGet(){


            }
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
                    "id": "6216559590087220004",            //委托订单ID
                    "clientOrderId": "16559590087220001",   //客户端订单号
                    "accountId": 123456,                    //账户ID
                    "userId": "123456",                     //用户ID
                    "symbolId": 1001,                       //交易对ID
                    "symbol": "BTC_USDT",                   //交易对名称
                    "side": "1",                            //订单方向 [1=买(BUY);2=卖(SELL)]
                    "type": "3",                            //订单类型 [3=ENTRUST_PROFIT(止盈止损);4=ENTRUST_TRACK(跟踪委托)]
                    "timeInForce": "1",                     //有效方式 [1=GTC;2=FOK;3=IOC;4=GTX;5=GTX_SELF_CANCEL]
                    "bizType": "1",                         //业务类型 [1=现货(SPOT)]
                    "price": "40000",                       //委托价格，止盈止损使用
                    "quantity": "2",                        //数量
                    "quoteQty": "48000",                    //金额，跟踪委托买入时输入
                    "triggerPrice": "41000",                //触发价格
                    "currentPrice": "40500",                //当前价格
                    "activePrice": "40000",                 //激活价格，跟踪委托使用（非必填）
                    "turnRate": "2",                        //回调幅度，跟踪委托使用
                    "priceDiff": "2",                       //价距，跟踪委托使用
                    "extremePrice": "40000",                //下单以来最高/最低价格（跟踪委托）：买入记录最低价，卖出记录最高价
                    "closed": false,                        //是否关闭
                    "closedTime": 1655971400834,            //关闭时间
                    "state": "1",                           //订单状态 [1=新建(NEW);2=已触发(TRIGGERED);3=已过期(EXPIRED);4=已撤销(CANCELED)]
                    "activeState": "0",                     //跟踪委托激活状态 [0=INACTIVE(未激活);1=ACTIVE(已激活)]
                    "triggerTime": 0,                       //触发限价单或市价单时间
                    "triggerState": "0",                    //下限价单或市价单结果 [0=NEW(新建);1=SUCCESS(成功);2=FAILED(失败)]
                    "rejectReason": "string",               //下单限价单或市价单失败原因
                    "ip": "127.0.0.1",                      //ip地址
                    "createdTime": 1655958915583,           //创建时间
                    "updatedTime": 1655958915583            //更新时间
                  }
                }
        title: Response
        language: json
---

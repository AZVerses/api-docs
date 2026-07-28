---
title: Get single entrust order
position_number: 16
type: get
description: /az/spot/entrust-order/{entrustOrderId}
parameters:
    -
        name: entrustOrderId
        type: number
        mandatory: true
        default:
        description: entrust order id
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
                    "id": "6216559590087220004",            //entrust order id
                    "clientOrderId": "16559590087220001",   //client order id
                    "accountId": 123456,                    //account id
                    "userId": "123456",                     //user id
                    "symbolId": 1001,                       //symbol id
                    "symbol": "BTC_USDT",                   //symbol
                    "side": "1",                            //order side [1=BUY;2=SELL]
                    "type": "3",                            //order type [3=ENTRUST_PROFIT;4=ENTRUST_TRACK]
                    "timeInForce": "1",                     //effective way [1=GTC;2=FOK;3=IOC;4=GTX;5=GTX_SELF_CANCEL]
                    "bizType": "1",                         //business type [1=SPOT]
                    "price": "40000",                       //entrust price, used by TP/SL
                    "quantity": "2",                        //quantity
                    "quoteQty": "48000",                    //amount, filled when tracking order buys
                    "triggerPrice": "41000",                //trigger price
                    "currentPrice": "40500",                //current price
                    "activePrice": "40000",                 //activation price, used by tracking order (optional)
                    "turnRate": "2",                        //callback rate, used by tracking order
                    "priceDiff": "2",                       //price distance, used by tracking order
                    "extremePrice": "40000",                //highest/lowest price since order (tracking order): lowest on buy, highest on sell
                    "closed": false,                        //whether closed
                    "closedTime": 1655971400834,            //closed time
                    "state": "1",                           //state [1=NEW;2=TRIGGERED;3=EXPIRED;4=CANCELED]
                    "activeState": "0",                     //tracking order active state [0=INACTIVE;1=ACTIVE]
                    "triggerTime": 0,                       //time when the limit/market order is triggered
                    "triggerState": "0",                    //result of placing the limit/market order [0=NEW;1=SUCCESS;2=FAILED]
                    "rejectReason": "string",               //reason for placing limit/market order failure
                    "ip": "127.0.0.1",                      //ip address
                    "createdTime": 1655958915583,           //created time
                    "updatedTime": 1655958915583            //updated time
                  }
                }
        title: Response
        language: json
---

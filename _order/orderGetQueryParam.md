---
title: Query single
position_number: 1
type: get
description: /az/spot/order
parameters:
    -
        name: orderId
        type: number
        mandatory: false
        default:
        description: 
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 
        ranges:
content_markdown:
left_code_blocks:
    -
        code_block: |-
            public String orderGet(){


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
                        "symbol": "BTC_USDT",   
                        "orderId": "6216559590087220004",  
                        "clientOrderId": "16559590087220001",  
                        "rfq": false,                       //whether it is an RFQ order
                        "baseCurrency": "string",   
                        "quoteCurrency": "string",   
                        "side": "BUY",                      //order side:BUY,SELL
                        "type": "LIMIT",                    //order type  LIMIT,MARKET 
                        "timeInForce": "GTC",               //effective way:GTC,IOC,FOK,GTX,GTX_SELF_CANCEL
                        "price": "40000",   
                        "origQty": "2",                     //original quantity
                        "origQuoteQty": "48000",            //original amount
                        "executedQty": "1.2",               //executed quantity
                        "leavingQty": "string",             //The quantity to be executed (if the order is cancelled or the order is rejected, the value is 0)
                        "tradeBase": "2",                   //transaction quantity
                        "tradeQuote": "48000",              //transaction amount
                        "avgPrice": "42350",                //average transaction price
                        "fee": "string",                    //handling fee
                        "feeCurrency": "string",   
                        "nftId": "string",                  //nft id
                        "symbolType": "normal",             //symbol type
                        "origRestFee": "string",            //remaining un-deducted fee in the original currency (including the coupon-deducted part)
                        "origFeeCurrency": "string",        //currency of the remaining un-deducted fee
                        "platFormCurrencyFee": "string",    //fee deducted by platform currency (e.g. xt)
                        "platFormCurrency": "string",       //platform currency
                        "couponAmount": "string",           //coupon amount used
                        "couponCurrency": "string",         //coupon currency
                        "couponDeductFee": "string",        //fee (in the original currency) deducted by the coupon
                        "closed": false,                    //whether closed
                        "state": "NEW",                     //order stat NEW,PARTIALLY_FILLED,FILLED,CANCELED,REJECTED,EXPIRED
                        "time": 1655958915583,              //order time
                        "updatedTime": 1655958915583  
                      }
                    }
        title: Response
        language: json
---

---
title: Alter Stop Limit
position_number: 12
type: post
description: /az/future/trade/v1/entrust/update-profit-stop
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
  - name: profitId
    type: integer
    mandatory: true
    default: N/A
    description: Stop limit ID
    ranges:
  - name: triggerProfitPrice
    type: number
    mandatory: false
    default: N/A
    description: TP trigger price
    ranges:
  - name: triggerStopPrice
    type: number
    mandatory: false
    default: N/A
    description: SL trigger price
    ranges:
  - name: triggerPriceType
    type: string
    mandatory: false
    default: N/A
    description: Trigger price type:INDEX_PRICE(Index price)；MARK_PRICE(Mark price)；LATEST_PRICE(latest price)
    ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
  - name: origQty
    type: number
    mandatory: false
    default: N/A
    description: Quantity (base coin)
    ranges:
  - name: closeType
    type: string
    mandatory: false
    default: N/A
    description: Close type:FIXED(Fixed);ALL(All)
    ranges: FIXED;ALL
  - name: profitDelegateOrderType
    type: string
    mandatory: false
    default: N/A
    description: TP delegate order type:LIMIT;MARKET
    ranges: LIMIT;MARKET
  - name: profitDelegateTimeInForce
    type: string
    mandatory: false
    default: N/A
    description: TP delegate time in force:GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
    ranges: GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
  - name: profitDelegatePrice
    type: number
    mandatory: false
    default: N/A
    description: TP delegate price
    ranges:
  - name: stopDelegateOrderType
    type: string
    mandatory: false
    default: N/A
    description: SL delegate order type:LIMIT;MARKET
    ranges: LIMIT;MARKET
  - name: stopDelegateTimeInForce
    type: string
    mandatory: false
    default: N/A
    description: SL delegate time in force:GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
    ranges: GTC;FOK;IOC;GTX;GTX_SELF_CANCEL
  - name: stopDelegatePrice
    type: number
    mandatory: false
    default: N/A
    description: SL delegate price
    ranges:
content_markdown: |-

                 #### **Limit Flow Rules**

                 200/s/apikey
right_code_blocks:
  - code_block: |-
      {
        "error": {
          "code": "",
          "msg": ""
        },
        "msgInfo": "",
        "result": {},
        "returnCode": 0
      }
    title: Response
    language: json
---
---
title: Get Market Information for All Trading Pairs
position_number: 8
type: get
description: /az/future/market/v1/public/q/tickers
parameters:
content_markdown: Note：This method does not require a signature.
left_code_blocks:
    -
        code_block: "public void getKLine() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/market/v1/getKLine?market=btc_usdt&type=1min&since=0\");\r\n\tSystem.out.println(text);\r\n}"
        title: Java
        language: java
right_code_blocks:
    - code_block: |-
        {
          "error": {
            "code": "",
            "msg": ""
          },
          "msgInfo": "success",
          "returnCode": 0,
          "result": [
            {
                "s": "btc_usdt",        //Trading pair
                "o": "109658.1",        //The first transaction price 24 hours ago
                "c": "109981.3",        //Latest price
                "h": "114308.1",        //Highest price in 24 hours
                "l": "108600.0",        //Lowest price in 24 hours
                "v": "3128038",         //24h transaction quantity (base)
                "uv": "34412784.72516", //24h transaction amount (quote)
                "r": "0.0029",          //24h Price Fluctuation Limit
                "bp": "110044.9",       //bid price (buy one price)
                "bq": "9667",           //bid qty (buy one quantity)
                "ap": "110045.0",       //ask price (sell one price)
                "aq": "13619",          //ask qty (sell one quantity)
                "ix": "109980.5",       //index price
                "mx": "109981.0",       //mark price
                "ts": 1761978054921     //Timestamp
            }
          ]
        }
      title: Response
      language: json
---
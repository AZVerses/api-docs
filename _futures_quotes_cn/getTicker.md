---
title: 获取指定交易对的行情信息
position_number: 7
type: get
description: /az/future/market/v1/public/q/ticker
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: 交易对
        ranges:
content_markdown: 注：**此方法不需要签名**
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
          "result": {
                "s": "btc_usdt",        //交易对
                "o": "109658.1",        //24小时前第一笔成交价
                "c": "109981.3",        //最新价
                "h": "114308.1",        //24小时最高价
                "l": "108600.0",        //24小时最低价
                "v": "3128038",         //24小时成交量(base 数量)
                "uv": "34412784.72516", //24小时成交额(quote 金额)
                "r": "0.0029",          //24小时涨跌幅
                "bp": "110044.9",       //买一价
                "bq": "9667",           //买一量
                "ap": "110045.0",       //卖一价
                "aq": "13619",          //卖一量
                "ix": "109980.5",       //指数价格
                "mx": "109981.0",       //标记价格
                "ts": 1761978054921     //时间
          }
        }
      title: Response
      language: json
---
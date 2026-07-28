---
title: 接口的基本信息
position_number: 2
parameters:
- name:
content:
content_markdown: >-
    鉴于延迟高和稳定性差等原因，不建议通过代理的方式访问API。


    GET请求参数放入query Params中，POST请求参数放入request body中


    请求头信息请设置为：Content-Type=application/x-www-form-urlencoded


    除了接口本身所需的参数外，签名 signature 需通过请求头 `validate-signature` 传递（不放在 query Params 或 request body 中），
    不需要传递签名参数的接口会额外说明。
left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---



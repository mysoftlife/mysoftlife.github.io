---
title: Place a New Order
position_number: 1.1
type: post
description: API Key Permission：Trade <br/>
             
parameters:
  - name: type
    content: limit_price or market_price (default is limit_price )
  - name: direction
    content: buy or sell
  - name: symbol
    content: A valid symbol：BTC-USDT
  - name: price
    content: Price per bitcoin (not available for market order)
  - name: amount
    content: Amount of base currency to buy or sell
content_markdown: |-
  The parameters must use RequestBody JSON
  {: .warning}

  You can place two types of orders: limit and market. Orders can only be placed if your account has sufficient funds.
left_code_blocks:
  - code_block: |-
      POST /v1.0/trades/spot/orders
      
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |-
     {
       "data": "T08128123000582660096",
       "code": "200",
       "message": "success"
     }
    title: Response
    language: json
  - code_block: |-
      {
        "data": null,
        "code": "400",
        "message": "error message here"
      }
    title: Error
    language: json
---



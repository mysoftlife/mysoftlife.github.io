---
title: Get Trades
position_number: 1.3
type: get
parameters:
  - name: size
    content: The number of data returns
content_markdown: |-
    List the latest trades for a symbol.
left_code_blocks:   
  - code_block: |-
      GET /v1.0/markets/{symbol}/trades
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
        "data": [
         {
          "symbol":"ETH-USDT", 
          "price":"1.0",
          "amount":"100.0"
          "buy_turnover":"100.0",
          "sell_turnover":"100.0",
          "direction":"BUY",
          "buy_order_id":"T08128123000582660096",
          "sell_order_id":"T08128123000582660098",
          "time":"1605166008"
         }],
        "code": 200,
        "message": "success"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "data": null,
        "code": "400",
        "message": "error message here"
      }
    title: Error
    language: json
---
---
title: List Trade History Orders
position_number: 1.8
type: get
description: API Key Permission：Read <br/>
             
parameters:
  - name: symbol
    content: The trading symbol to trade
  - name: type
    content: market_price|limit_price|all
  - name: start_time
    content: the start timestamp
  - name: end_time
    content: the end timestamp
  - name: direction
    content: sell|buy|all,Filter on the direction of the trade
  - name: limit
    content: Default 500; max 1000.
content_markdown: |-
  List your trade historical orders from the profile that the API key belongs to. Only completed orders are returned.
left_code_blocks:
  - code_block: |-
           GET /v1.0/trades/spot/orders/trade-history
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
        "data": {
            "total_pages": 1, 
            "total_elememts":10，
            "content": [
            {
             "order_id":"T08128123000582660096",
               "member_id":"1",
               "type":"LIMIT_PRICE",
               "amount":"100.0"
               "symbol":"BTC-USDT",
               "symbol_display_name":"BTC/USDT",
               "trade_amount":"100.0",
               "trunover":"100.0",
               "coin_symbol":"BTC",
               "base_symbol":"USDT",
               "status":"TRADING",
               "direction":"BUY",
               "price":"1.0",
               "time":"1605166008",
               "completed_time":"1605166008",
               "canceled_time":"1605166008",
               "use_discount":"0",
               "order_detail":
                 [{
                  "order_id":"T08128123000582660096",
                  "price":"1.0",
                  "amount":"100.0",
                  "tunover":"100.0",
                  "fee":"0.1",
                  "time":"1605166008"
                 }]
            }
          ]
        }, 
        "code": "200", 
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
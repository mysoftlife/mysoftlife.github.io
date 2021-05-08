---
title: Get an Order
position_number: 1.3
type: get
description: API Key Permission：Read <br/>
            
parameters:
  - name: 
    content:
content_markdown: |-
  Open orders may change state between the request and the response depending on market conditions.
  {: .info }

  Get a single order by order id from the profile that the API key belongs to.
left_code_blocks:
  - code_block: |-
      GET /v1.0/trades/spot/orders/{orderId}
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
        "data": {
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
           "order_detail":[{
                 "order_id":"T08128123000582660096",
                 "price":"1.0",
                 "amount":"100.0",
                 "tunover":"100.0",
                 "fee":"0.1",
                 "time":"1605166008"
           }]
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
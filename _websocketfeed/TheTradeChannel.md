---
title: The Trade Channel
position_number: 1.4
parameters:
  - name:
    content:
content_markdown: |-
    This topic sends the latest completed trade. It updates in tick by tick mode.
  
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |2-
        {
          "type": "subscribe",
          "channels": [
              {
                "name": "trade",
                "symbol": "ETH-USDT"
              }
          ]
        }
    title: Subscribe
    language: json
  - code_block: |2-
      {
        "symbol":"ETH-USDT", 
        "price":"1.0",
        "amount":"100.0"
        "buy_turnover":"100.0",
        "sell_turnover":"100.0",
        "direction":"BUY",//BUY,SELL
        "buy_order_id":"T08128123000582660096",
        "sell_order_id":"T08128123000582660098",
        "time":"1605166008"
      }
    title: Push Data
    language: json
---
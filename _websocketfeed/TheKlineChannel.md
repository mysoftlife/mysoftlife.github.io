---
title: The Kline Channel
position_number: 1.2
parameters:
  - name:
    content:
content_markdown: |-
    This topic sends a new candlestick whenever it is available.
  
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
                "name": "kline",
                "symbol": "ETH-USDT",
                "period": "1h" //min,hour,day,week,month
              }
          ]
        }
    title: Subscribe
    language: json
  - code_block: |2-
        {
          "symbol": "ETH-USDT",
          "time": "1605787212",
          "open_price":"0.2",
          "highest_price":0.2,
          "lowest_price":0.3,
          "close_price":0.1, 
          "period":0.1,
          "count":0.5,
          "volume":1.0,
          "turnover": 10.0
        }
    title: Push Data
    language: json
---
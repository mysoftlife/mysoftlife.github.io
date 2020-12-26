---
title: The Depth Channel
position_number: 1.3
parameters:
  - name:
    content:
content_markdown: |-
    This topic sends the latest market by price order book in snapshot mode at 1-minute interval.
  
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
                "name": "depth",
                "symbol": "ETH-USDT",
                "scale": "0.01"
              }
          ]
        }
    title: Subscribe
    language: json
  - code_block: |2-
      {
          "symbol": "ETH-USDT",
          "symbol_display_name": "ETH/USDT",
          "min_amount": 2.00000000,
          "lowest_price": 0.04000000,
          "max_amount": 10.00000000,
          "highest_price": 0.06000000,
          "items": [
              {
                  "amount": 10.00000000,
                  "price": 0.04
              }
          ],
          "direction": "SELL"
      }
    title: Push Data
    language: json
---
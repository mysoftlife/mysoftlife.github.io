---
title: The Ticker Channel
position_number: 1.5
parameters:
  - name:
    content:
content_markdown: |-
    Pushes any update to the best bid or ask's price or quantity in real-time for all symbols.
  
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
                "name": "ticker",
                "symbol": "ETH-USDT",
                "scale": "0.01"
              }
          ]
        }
    title: Subscribe
    language: json
  - code_block: |2-
      {
          "ask": {
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
          },
          "bid": {
              "symbol": "ETH-USDT",
              "symbol_display_name": "ETH/USDT",
              "min_amount": 1733.00000000,
              "lowest_price": 0.01000000,
              "max_amount": 1733.00000000,
              "highest_price": 0.01000000,
              "items": [
                  {
                      "amount": 1733.00000000,
                      "price": 0.01
                  }
              ],
              "direction": "BUY"
          }
      }
          
    title: Push Data
    language: json
---
---
title: Subscribe
position_number: 1.1
parameters:
  - name:
    content:
content_markdown: |-
    To begin receiving feed messages, you must first send a subscribe message to the server indicating which channels and products to receive. This message is mandatory — you will be disconnected if no subscribe has been received within 5 seconds.
  
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |2-
        // Request
        {
          "type": "subscribe",
          "symbols": [
              "ETH-USD",
              "ETH-EUR"
          ],
          "channels": [
              "heartbeat",
              {
                "name": "klines",
                "symbols": [
                    "ETH-BTC",
                    "ETH-USD"
                ]
              }
          ]
        }
    title: Subscribe
    language: json
  - code_block: |2-
      // Request
      {
        "type": "unsubscribe",
        "symbols": [
            "ETH-USD",
            "ETH-EUR"
        ],
        "channels": ["klines"]
      }
    title: Unsubscribe
    language: json
---
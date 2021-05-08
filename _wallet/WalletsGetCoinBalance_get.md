---
title: Wallets get coin balance
position_number: 5
type: get
description: API Key Permission：Wallet <br/>
             
parameters:
  - name: 
    content: 
content_markdown: |-
  Get user coin balance.
left_code_blocks:
  - code_block: |-
       GET  /v1.0/wallets/coins
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
       {
         "data": [
           {
             "symbol": "ETH", 
             "available_amount": "17485388032.4", 
             "locked_amount": "0"
           }
         ], 
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
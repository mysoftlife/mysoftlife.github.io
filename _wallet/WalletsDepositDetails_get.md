---
title: Wallets deposit details
position_number: 3
type: get
description: API Key Permission：Wallet <br/>
             Rate Limit (NEW):50times/2s
parameters:
  - name: symbol
    content: coin symbol example:USDT, ETH , All
content_markdown: |-
  Get the user's inbound address information.
left_code_blocks:
  - code_block: |-
       GET  /v1.0/wallets/coins/{symbol}/deposit
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
       {
         "data": {
           "symbol": "USDT", 
           "network_list": [
             {
               "address": "address", 
               "memo": "E3JS", 
               "min_deposit_amount": "1", 
               "network": "ERC20", 
               "confirmation": 12, 
               "can_deposit": true
             }, 
             {
               "address": "address", 
               "memo": "E3JS", 
               "min_deposit_amount": "0.1", 
               "network": "OMNI", 
               "confirmation": 12, 
               "can_deposit": false
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
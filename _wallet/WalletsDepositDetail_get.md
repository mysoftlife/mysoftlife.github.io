---
title: Wallets deposit detail
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
         "code": "200", 
         "data": {
           "name": "Tether", 
           "symbol": "USDT", 
           "icon_url": "url", 
           "network_list": [
             {
               "address": "address", 
               "min_deposit_amount": "1", 
               "network_name": "ERC20", 
               "confirmation": 12
             }, 
             {
               "address": "address", 
               "min_deposit_amount": "0.1", 
               "network_name": "OMNI", 
               "confirmation": 12
             }
           ]
         }, 
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
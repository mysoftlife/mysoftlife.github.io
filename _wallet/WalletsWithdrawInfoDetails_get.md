---
title: Wallets withdraw info details
position_number: 2
type: get
description: API Key Permission：Wallet <br/>
             Rate Limit (NEW):50times/2s
parameters:
  - name: symbol
    content: coin symbol example:USDT, ETH , All
content_markdown: |-
  Gets information about the amount of money that can be transferred out in a given currency.
left_code_blocks:
  - code_block: |-
       GET  /v1.0/wallets/coins/{symbol}/withdrawal
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
       {
         "code": "200", 
         "data": {
           "available_amount": "0.00000000", 
           "locked_amount": "0.00000000", 
           "name": "Tether", 
           "icon_url": "url", 
           "network_list": [
             {
               "withdraw_scale": 8, 
               "available_amount": "0.00000000", 
               "min_withdraw_amount": "0.00000000", 
               "network_id": 1, 
               "network_name": "Ethereum Mainnet", 
               "transaction_fee": "0.00000000"
             }
           ], 
           "symbol": "ETH", 
           "total_amount": "0.00000000"
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
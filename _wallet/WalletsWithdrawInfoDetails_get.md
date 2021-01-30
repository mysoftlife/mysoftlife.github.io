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
           "data": {
               "symbol": "USDT",
               "network_list": [
                   {
                       "network_name": "ERC20",
                       "min_withdraw_amount": "10",
                       "transaction_fee": "5",
                       "network_type": "address",     
                       "withdraw_scale": 6,               
                       "can_withdrawal": true         
                   },
                   {
                       "network_name": "OMNI",
                       "min_withdraw_amount": "200",
                       "transaction_fee": "5",
                       "network_type": "address",
                       "withdraw_scale": 6,
                       "can_withdrawal": true
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
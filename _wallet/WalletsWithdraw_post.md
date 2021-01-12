---
title: Wallets withdraw
position_number: 1
type: post
description: API Key Permission：Wallet <br/>
             Rate Limit (NEW):50times/2s
parameters:
  - name: symbol
    content: coin symbol example:USDT, ETH , All
content_markdown: |-
  The parameters must use RequestBody JSON
  {: .warning}
  
  RequestBody:
  ```json
    {
      "withdraw_amount": "10",
      "address": "0x8a9fcb56aabe5d828c23477b7b60e6e5b481a108",
      "network_id": 1
    }
  ```


  The withdrawal api.
left_code_blocks:
  - code_block: |-
       POST  /v1.0/wallets/coins/{symbol}/withdrawal
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
       {
         "data": {
           "id": 74, 
           "time": "2020-11-12 09:00:14", 
           "symbol": "USDT", 
           "amount": "10.00000000", 
           "address": "0x8a9fcb56aabe5d828c23477b7b60e6e5b481a108", 
           "txid": "", 
           "status": "Auditing", 
           "network_confirmation": "0/12", 
           "type": "withdraw", 
           "transaction_fee": "11"
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
---
title: Wallets History
position_number: 1
type: get
description: API Key Permission：Wallet <br/>
             Rate Limit (NEW):50times/2s
parameters:
  - name: user_id
    content: The userid for account 
  - name: symbol
    content: coin symbol example:USDT, ETH , All
  - name: transaction_type
    content: The transaction_type Example:all, deposit, withdrawal, transfer
  - name: start_data
    content: the query start date  example:2020-11-12, all
  - name: end_data
    content: the query end date  example:2020-11-20, all
  - name: page_no
    content: the query page number(start from 0)
  - name: sage_size
    content: the query page size 
content_markdown: |-
  This request is paginated.
  {: .info }
  The transaction history of the wallet can be searched according to different currencies and different types.
left_code_blocks:
  - code_block: |-
       GET /v1.0/wallets/transaction-history
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
       {
         "data": {
           "transaction_history_list": [
             {
               "type": "transfer", 
               "id": 180, 
               "time": "2020-12-09 13:08:24", 
               "symbol": "ETH", 
               "amount": "123", 
               "status": "Completed", 
               "network_name": "ETH", 
               "description": "Reissued"
             }, 
             {
               "type": "withdrawal", 
               "id": 179, 
               "time": "2020-12-07 20:51:04", 
               "symbol": "USDT", 
               "amount": "100000000", 
               "address": "0xcc7dc3f8cf73916005439e22ce269a718b3a03cd", 
               "txid": "0xc0851f97dcc49e3cc7153ec7cdaeecf209392936f971a7f42cd4c8db70c94536", 
               "status": "Completed", 
               "network_confirmation": "12/12", 
               "network_name": "ERC20", 
               "transaction_fee": "0"
             }
           ], 
           "total_page": 24, 
           "total_number": 48
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
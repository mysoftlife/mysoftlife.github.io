---
title: Wallet coin list
position_number: 5
type: get
description: API Key Permission：Wallet <br/>
             Rate Limit (NEW):50times/2s
parameters:
  - name: 
    content: 
content_markdown: |-
  Get supported coins.
left_code_blocks:
  - code_block: |-
       GET  /v1.0/coins
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
       {
         "code": "200", 
         "data": [
           {
             "name": "Ethereum", 
             "symbol": "ETH"
           }
         ], 
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
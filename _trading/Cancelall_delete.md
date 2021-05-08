---
title: Cancel all
position_number: 1.5
type: delete
description: API Key Permission：Trade <br/>
             
parameters:
  - name: symbol
    content: The trading symbol
content_markdown: |-
  The response was the number of cancellations.
  {: .info }
  
  With best effort, cancel all open orders from the profile that the API key belongs to.
left_code_blocks:
  - code_block: |-
     DELETE /v1.0/trades/spot/orders
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
        "data": {success:3,failure:1},
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


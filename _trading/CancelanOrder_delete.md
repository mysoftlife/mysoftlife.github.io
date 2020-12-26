---
title: Cancel an Order
position_number: 1.4
type: delete
description: API Key Permission：Trade <br/>
             Rate Limit (NEW):50times/2s
parameters:
  - name: 
    content: 
content_markdown: |-
  If the order could not be canceled (already filled or previously canceled, etc), then an error response will indicate the reason in the message field.
  {: .warning }
  
  Cancel a previously placed order. Order must belong to the profile that the API key belongs to.
left_code_blocks:
  - code_block: |-
     DELETE /v1.0/trades/spot/orders/{orderId}
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
        "data": 1,
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
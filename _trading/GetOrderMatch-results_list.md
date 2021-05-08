---
title: Get Order Match-results
position_number: 1.9
type: get
description: API Key Permission：Read <br/>
             
parameters:
  - name: 
    content: 
content_markdown: |-
  The return data contains a list and each item in the list represents a match result.
  {: .info }

  This endpoint returns the match results of past and open orders based on specific search criteria.
left_code_blocks:
  - code_block: |-
           GET /v1.0/trades/spot/orders/{orderId}/match-results
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
         "code": "200",
         "message": "success",
         "data": [{
            order_id:"T08128123000582660096",
            amount:"1000.0",
            price:"10.0",
            turnover:"100.0",
            fee:"0.2",
            time:"1605164996"
          }]
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
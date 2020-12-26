---
title: Get Klines
position_number: 1.4
type: get
parameters:
  - name: from
    content: The start time.
  - name: to
    content: The end time.
  - name: resolution
    content: min,hour,day,week,month<br/>
             example：<br/>
             50,24h,1d,1w,1m<br/>
             Minutes don't need units
content_markdown: |-
    If startTime and endTime are not sent, the most recent klines are returned.
    {: .info }
    
    This endpoint retrieves all klines in a specific range.
left_code_blocks:   
  - code_block: |-
      GET /v1.0/markets/{symbol}/klines
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
         "data":[
          {
            "0":"1605787212",//time
            "1":0.2,         //open
            "2":0.3,         //heigh
            "3":0.1,         //low
            "4":0.1,         //close
            "5":0.5          //volume
           }
          ], 
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
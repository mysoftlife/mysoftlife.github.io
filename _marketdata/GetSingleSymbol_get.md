---
title: Get Single Symbol
position_number: 1.1
type: get
parameters:
  - name: 
    content: 
content_markdown: |-
  Get market data for a specific currency pair.
left_code_blocks:   
  - code_block: |-
      GET /v1.0/markets/symbols/{symbol}
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
        "data": {
           symbol:"ETH-USDT",                
           display_name:"ETH/USDT",          
           coin_symbol:"ETH",                
           base_symbol:"USDT",              
           enable:1,                        
           fee:0.01,                        
           sort:1,                           
           coin_scale:1,                     
           base_coin_scale:1,               
           min_sell_price:0.1,               
           max_buy_price:0.2,                
           enable_market_sell:1,           
           enable_market_buy:1,           
           max_trading_time:1605787212,     
           max_trading_order:10001,          
           robot_type:0,                     
           flag:0,
           min_turnover:0,                   
           zone:1,                          
           min_volume:100.0,                 
           max_volume:100.0,                 
           publish_type:1,                   
           start_time:"2000-01-01 01:00:00", 
           end_time:"2000-01-01 01:00:00",  
           clear_time:"2000-01-01 01:00:00",
           publish_price:0.01,              
           publish_amount:0.01,              
           visible:1,                       
           exchangeable:1                   
          },
         "code": 200, 
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
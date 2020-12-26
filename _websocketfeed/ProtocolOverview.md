---
title: Protocol overview
position_number: 1.0
parameters:
  - name:
    content:
content_markdown: |-
  The websocket feed uses a bidirectional protocol, which encodes all messages as JSON objects. All messages have a type attribute that can be used to handle the message appropriately.<br/>
  Please note that new message types can be added at any point in time. Clients are expected to ignore messages they do not support.<br/>
  
  The websocket feed provides real-time market data updates for orders and trades.<br/>
   {: .info }
  
left_code_blocks:
  - code_block:
      wss://ws-feed.powx.com
    title: WSS
    language: javascript
right_code_blocks:
  - code_block:
    title:
    language:
---
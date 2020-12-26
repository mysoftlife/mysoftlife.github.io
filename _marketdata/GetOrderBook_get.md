---
title: Get Order Book
position_number: 1.2
type: get
parameters:
  - name: type
    content: Select response detail. Valid types are documented below.
  - name: scale
    content: the scale default is 0.00000001
content_markdown: |-
    <table><thead>
    <tr>
    <th>Type</th>
    <th>Description</th>
    </tr>
    </thead><tbody>
    <tr>
    <td>all</td>
    <td>Only the best bid and ask</td>
    </tr>
    <tr>
    <td>mini</td>
    <td>Top 50 bids and asks (aggregated)</td>
    </tr>
    <tr>
    <td>full</td>
    <td>Full order book (non aggregated)</td>
    </tr>
    </tbody></table>
    Get a list of open orders for a symbol.
left_code_blocks:   
  - code_block: |-
      GET /v1.0/markets/{symbol}/order-book
    title: HTTP REQUEST
    language: java
right_code_blocks:
  - code_block: |2-
      {
      "data": {
          "ask": {
              "symbol": "ETH-USDT",
              "symbol_display_name": "ETH/USDT",
              "min_amount": 2.00000000,
              "lowest_price": 0.04000000,
              "max_amount": 10.00000000,
              "highest_price": 0.06000000,
              "items": [
                  {
                      "amount": 10.00000000,
                      "price": 0.04000000
                  }
              ],
              "direction": "SELL"
          },
          "bid": {
              "symbol": "ETH-USDT",
              "symbol_display_name": "ETH/USDT",
              "min_amount": 1733.00000000,
              "lowest_price": 0.01000000,
              "max_amount": 1733.00000000,
              "highest_price": 0.01000000,
              "items": [
                  {
                      "amount": 1733.00000000,
                      "price": 0.01000000
                  }
              ],
              "direction": "BUY"
          }
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
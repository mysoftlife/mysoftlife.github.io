---
title: Errors
position_number: 2
parameters:
  - name:
    content:
content_markdown: |-
  
  <p>Unless otherwise stated, errors to bad requests will respond with HTTP 4xx or status codes. The body will also contain a <code>message</code> parameter indicating the cause. Your language's http library should be configured to provide message bodies for non-2xx requests so that you can read the message field from the body.</p>
  <p>Common error codes</p>
  <table><thead>
  <tr>
  <th>Status Code</th>
  <th>Reason</th>
  </tr>
  </thead><tbody>
  <tr>
  <td>400</td>
  <td>Bad Request -- Invalid request format</td>
  </tr>
  <tr>
  <td>401</td>
  <td>Unauthorized -- Invalid API Key</td>
  </tr>
  <tr>
  <td>403</td>
  <td>Forbidden -- You do not have access to the requested resource</td>
  </tr>
  <tr>
  <td>404</td>
  <td>Not Found</td>
  </tr>
  <tr>
  <td>500</td>
  <td>Internal Server Error -- We had a problem with our server</td>
  </tr>
  </tbody></table>
left_code_blocks:
  - code_block: 
    title: 
    language: 
right_code_blocks:
  - code_block: |-
                     {
                       "data": null,
                       "code": 400,
                       "message": "error message here"
                     }
    title:
    language:
---
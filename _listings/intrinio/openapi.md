swagger: "2.0"
x-collection-name: Intrinio
x-complete: 1
info:
  title: Intrinio
  version: 1.0.0
host: api.intrinio.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /securities/institutional_ownership:
    get:
      summary: Institutional Owners by Security
      description: https://api.intrinio.com/securities/institutional_ownership?identifier={symbol}
      operationId: institutional-owners-by-security
      x-api-path-slug: securitiesinstitutional-ownership-get
      parameters:
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities or the Central Index Key issued by the SEC, which
          is the unique identifier all company filings are issued under:'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Securities
      - Institutional Ownership
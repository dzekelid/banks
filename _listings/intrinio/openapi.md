---
swagger: "2.0"
x-collection-name: Intrinio
x-complete: 1
info:
  title: Intrinio
  description: through-our-intrinio-data-marketplace-we-offer-a-wide-selection-of-financial-data-feeds-sourced-by-our-own-proprietary-processes-as-well-as-from-many-data-vendors--the-primary-application-of-the-intrinio-api-is-for-use-in-thirdparty-applications-and-integrations-or-for-endusers-utilizing-the-excel-addin-and-google-sheets-addon--the-intrinio-api-uses-https-verbs-and-a-restful-endpoint-structure-which-makes-it-easy-to-request-data-from-intrinio--basic-authentication-is-administered-over-https--responses-are-delivered-in-json-format-
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
  /banks/holding_companies:
    get:
      summary: Bank Holding Companies
      description: Returns bank holding company list and information for all bank
        holding companies covered by Intrinio.
      operationId: bank-holding-companies
      x-api-path-slug: banksholding-companies-get
      parameters:
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
      - in: query
        name: query
        description: used to search for a ticker or bank name to return relevant banks
        type: string
      - in: query
        name: rssd_id
        description: 'the bank/bank holding company RSSD ID issued by the Federal
          Reserve: RSSD ID LOOKUP'
        type: string
      - in: query
        name: ticker
        description: 'the stock market ticker symbol associated with the companies
          common stock securities:'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Holding Companies
      - Banks
  /banks/failed:
    get:
      summary: Failed Banks
      description: Returns failed bank list and information for all failed banks covered
        by Intrinio.
      operationId: failed-banks
      x-api-path-slug: banksfailed-get
      parameters:
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
      - in: query
        name: query
        description: used to search for a bank name to return relevant failed banks
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Failed Banks
  /tags/banks:
    get:
      summary: Bank XBRL Tags and Labels
      description: Returns the Bank XBRL tags and labels for a given ticker/RSSD ID,
        statement, and date or fiscal year/fiscal quarter.
      operationId: bank-xbrl-tags-and-labels
      x-api-path-slug: tagsbanks-get
      parameters:
      - in: query
        name: fiscal_period
        description: 'the fiscal period associated with the fundamental: FY | Q1 |
          Q2 | Q3 | Q4 | Q1TTM | Q2TTM | Q3TTM | Q2YTD | Q3YTD'
        type: string
      - in: query
        name: fiscal_year
        description: 'the fiscal year associated with the fundamental: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities, or the bank/bank holding company RSSD ID issued
          by the Federal Reserve:'
        type: string
      - in: query
        name: item
        description: in function)
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
      - in: query
        name: sequence
        description: an integer 0 or greater for calling a single tag from the first
          entry
        type: string
      - in: query
        name: statement
        description: the financial statement requested from the call report, the UBPR
          report or Y
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Banks
---
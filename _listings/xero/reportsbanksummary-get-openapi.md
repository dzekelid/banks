---
swagger: "2.0"
x-collection-name: Xero
x-complete: 0
info:
  title: Clarity Accounting Get Reports Banksummary
  description: Get reports banksummary.
  contact:
    name: Xero Developer Team
    url: https://developer.xero.com
  version: "2.0"
host: api.xero.com
basePath: /api.xro/2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Reports/BankStatement:
    get:
      summary: Get Reports Bankstatement
      description: Get reports bankstatement.
      operationId: getReportsBankstatement
      x-api-path-slug: reportsbankstatement-get
      parameters:
      - in: query
        name: bankAccountID
        description: bankAccountID e
      - in: query
        name: fromDate
        description: YYYY-MM-DD
      - in: query
        name: toDate
        description: YYYY-MM-DD
      responses:
        200:
          description: OK
      tags:
      - Reports
      - BankStatement
    x-related-model:
      summary: X-related-model Reports Bankstatement
      description: X-related-model reports bankstatement.
      operationId: x-related-modelReportsBankstatement
      x-api-path-slug: reportsbankstatement-xrelatedmodel
      responses:
        200:
          description: OK
      tags:
      - Reports
      - BankStatement
  /Reports/BankSummary:
    get:
      summary: Get Reports Banksummary
      description: Get reports banksummary.
      operationId: getReportsBanksummary
      x-api-path-slug: reportsbanksummary-get
      parameters:
      - in: query
        name: fromDate
        description: YYYY-MM-DD
      - in: query
        name: toDate
        description: YYYY-MM-DD
      responses:
        200:
          description: OK
      tags:
      - Reports
      - BankSummary
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
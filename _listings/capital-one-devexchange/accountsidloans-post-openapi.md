---
swagger: "2.0"
x-collection-name: Capital One DevExchange
x-complete: 0
info:
  title: Capital One DevExchange Create a loan
  description: Creates a loan where the account with the ID specified is debitted.
  version: 1.0.0
host: api.reimaginebanking.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts:
    get:
      summary: Get all accounts
      description: Returns the accounts that have been assigned to you.
      operationId: returns-the-accounts-that-have-been-assigned-to-you
      x-api-path-slug: accounts-get
      parameters:
      - in: query
        name: type
        description: Empty Param will return all types of accounts
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
  /accounts/{id}:
    get:
      summary: Get account by id
      description: Returns the account with the specific id
      operationId: returns-the-account-with-the-specific-id
      x-api-path-slug: accountsid-get
      parameters:
      - in: path
        name: id
        description: ID of account that needs to be fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
    put:
      summary: Update a specific existing account
      description: Updates the specific account
      operationId: updates-the-specific-account
      x-api-path-slug: accountsid-put
      parameters:
      - in: body
        name: body
        description: Updated account object
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: ID of account that needs to be fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
    delete:
      summary: Delete a specific existing account
      description: Deletes the specific account
      operationId: deletes-the-specific-account
      x-api-path-slug: accountsid-delete
      parameters:
      - in: path
        name: id
        description: ID of account that needs to be fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
  /customers/{id}/accounts:
    post:
      summary: Create an account
      description: Creates an account for the customer with the id provided
      operationId: creates-an-account-for-the-customer-with-the-id-provided
      x-api-path-slug: customersidaccounts-post
      parameters:
      - in: body
        name: body
        description: Account to be created
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: ID of customer that account will belong to
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Customers
      - ""
      - Accounts
    get:
      summary: Get accounts by customer id
      description: Returns the accounts associated with the specific customer
      operationId: returns-the-accounts-associated-with-the-specific-customer
      x-api-path-slug: customersidaccounts-get
      parameters:
      - in: path
        name: id
        description: ID of customer to fetch accounts for
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Customers
      - ""
      - Accounts
  /accounts/{id}/customer:
    get:
      summary: Get customer that owns the specified account
      description: Returns the customer that the account belongs to.
      operationId: returns-the-customer-that-the-account-belongs-to
      x-api-path-slug: accountsidcustomer-get
      parameters:
      - in: path
        name: id
        description: ID of customer that account will belong to
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
      - ""
      - Customer
  /atms:
    get:
      summary: Get all ATMs
      description: Returns all of the Capital One ATMs in the speified search area.
      operationId: returns-all-of-the-capital-one-atms-in-the-speified-search-area
      x-api-path-slug: atms-get
      parameters:
      - in: query
        name: lat
        description: Latitude of where youre looking for an ATM
      - in: query
        name: lng
        description: Longitude of where youre looking for an ATM
      - in: query
        name: rad
        description: Search radius in miles
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Atms
  /atms/{id}:
    get:
      summary: Get ATM by id
      description: Returns the ATM with the specific id
      operationId: returns-the-atm-with-the-specific-id
      x-api-path-slug: atmsid-get
      parameters:
      - in: path
        name: id
        description: ID of ATM that needs to be fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Atms
  /accounts/{id}/bills:
    get:
      summary: Get all bills for a specific account
      description: Returns the bills that are tied to the specific account.
      operationId: returns-the-bills-that-are-tied-to-the-specific-account
      x-api-path-slug: accountsidbills-get
      parameters:
      - in: path
        name: id
        description: ID of account to fetch bills for
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
      - ""
      - Bills
    post:
      summary: Create a bill
      description: Creates a bill for the specific account
      operationId: creates-a-bill-for-the-specific-account
      x-api-path-slug: accountsidbills-post
      parameters:
      - in: body
        name: body
        description: Bill to be created
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: ID of account that the bill will belong to
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
      - ""
      - Bills
  /bills/{billId}:
    get:
      summary: Get bill by id
      description: Returns the bill with the specific id
      operationId: returns-the-bill-with-the-specific-id
      x-api-path-slug: billsbillid-get
      parameters:
      - in: path
        name: billId
        description: ID of the bill to fetch
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Bills
      - Bill
    put:
      summary: Update a specific existing bill
      description: Updates the specific bill
      operationId: updates-the-specific-bill
      x-api-path-slug: billsbillid-put
      parameters:
      - in: path
        name: billId
        description: ID of the bill to update
      - in: body
        name: body
        description: Bill to be updated
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Bills
      - Bill
    delete:
      summary: Delete a specific existing bill
      description: Deletes the specific bill
      operationId: deletes-the-specific-bill
      x-api-path-slug: billsbillid-delete
      parameters:
      - in: path
        name: billId
        description: ID of the bill to delete
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Bills
      - Bill
  /branches:
    get:
      summary: Get all branches
      description: Returns all of the Capital One branches.
      operationId: returns-all-of-the-capital-one-branches
      x-api-path-slug: branches-get
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Branches
  /branches/{id}:
    get:
      summary: Get branch by id
      description: Returns the branch with the specific id
      operationId: returns-the-branch-with-the-specific-id
      x-api-path-slug: branchesid-get
      parameters:
      - in: path
        name: id
        description: ID of branch that needs to be fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Branches
  /customers:
    get:
      summary: Get all customers
      description: Returns the customers that have been assigned to you.
      operationId: returns-the-customers-that-have-been-assigned-to-you
      x-api-path-slug: customers-get
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Customers
    post:
      summary: Create a customer
      description: Creates a customer
      operationId: creates-a-customer
      x-api-path-slug: customers-post
      parameters:
      - in: body
        name: body
        description: Customer to be created
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Customers
  /customers/{id}:
    get:
      summary: Get customer by id
      description: Returns the customer with the specific id
      operationId: returns-the-customer-with-the-specific-id
      x-api-path-slug: customersid-get
      parameters:
      - in: path
        name: id
        description: ID of customer that needs to be fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Customers
    put:
      summary: Update a specific existing customer
      description: Updates the specific customer
      operationId: updates-the-specific-customer
      x-api-path-slug: customersid-put
      parameters:
      - in: body
        name: body
        description: Updated customer object
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: ID of customer that needs to be fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Customers
  /customers/{id}/bills:
    get:
      summary: Get bills by customer id
      description: Returns the bills associated with the specific customer
      operationId: returns-the-bills-associated-with-the-specific-customer
      x-api-path-slug: customersidbills-get
      parameters:
      - in: path
        name: id
        description: ID of customer to fetch bills for
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Customers
      - ""
      - Bills
  /data:
    delete:
      summary: Delete data associated with your API key.
      description: This endpoint deletes any data associated with your API key and
        of the type passed in as query parameters.  If you do not specify any type
        to delete, no data will be deleted.
      operationId: this-endpoint-deletes-any-data-associated-with-your-api-key-and-of-the-type-passed-in-as-query-param
      x-api-path-slug: data-delete
      parameters:
      - in: query
        name: type
        description: Collection to delete data from
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Data
  /accounts/{id}/deposits:
    get:
      summary: Get all deposits
      description: Returns the deposits that you are involved in.
      operationId: returns-the-deposits-that-you-are-involved-in
      x-api-path-slug: accountsiddeposits-get
      parameters:
      - in: path
        name: id
        description: ID of account associated with the deposit
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
      - ""
      - Deposits
    post:
      summary: Create a deposit
      description: Creates a deposit where the account with the ID specified receives
        the amount.
      operationId: creates-a-deposit-where-the-account-with-the-id-specified-receives-the-amount
      x-api-path-slug: accountsiddeposits-post
      parameters:
      - in: body
        name: body
        description: Deposit to be created
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: ID of account receiver of deposit
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
      - ""
      - Deposits
  /deposits/{id}:
    get:
      summary: Get deposit by id
      description: Returns the deposit with the specific id
      operationId: returns-the-deposit-with-the-specific-id
      x-api-path-slug: depositsid-get
      parameters:
      - in: path
        name: id
        description: ID of the deposit that is being fetched
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Deposits
    put:
      summary: Update a specific existing deposit
      description: Updates the specific deposit
      operationId: updates-the-specific-deposit
      x-api-path-slug: depositsid-put
      parameters:
      - in: body
        name: body
        description: deposit to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: ID of the deposit that is being updated
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Deposits
    delete:
      summary: Delete a specific existing deposit
      description: Deletes the specific deposit
      operationId: deletes-the-specific-deposit
      x-api-path-slug: depositsid-delete
      parameters:
      - in: path
        name: id
        description: ID of the deposit that is being deleted
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Deposits
  /accounts/{id}/loans:
    get:
      summary: Get all loans
      description: Returns the loans that you are involved in.
      operationId: returns-the-loans-that-you-are-involved-in
      x-api-path-slug: accountsidloans-get
      parameters:
      - in: path
        name: id
        description: ID of account associated with the loan
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
      - ""
      - Loans
    post:
      summary: Create a loan
      description: Creates a loan where the account with the ID specified is debitted.
      operationId: creates-a-loan-where-the-account-with-the-id-specified-is-debitted
      x-api-path-slug: accountsidloans-post
      parameters:
      - in: body
        name: body
        description: loan to be created
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: ID of account receiver of loan
      responses:
        200:
          description: OK
      tags:
      - Banks
      - Accounts
      - ""
      - Loans
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
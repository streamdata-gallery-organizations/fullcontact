---
swagger: "2.0"
x-collection-name: FullContact
x-complete: 0
info:
  title: FullContact Get Icons
  description: Get Icons
  termsOfService: https://www.fullcontact.com/terms/
  version: 1.0.0
host: api.fullcontact.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /batch.json:
    get:
      summary: Batch Process
      description: Batch Process
      operationId: batchProcess
      x-api-path-slug: batchjson-get
      parameters:
      - in: query
        name: apiKey
        description: This API key is assigned to you by FullContact
      - in: body
        name: Body
        description: '{     requests : [         https://api'
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Batch
  /stats.json:
    get:
      summary: Get Account Stats
      description: Get Account Stats
      operationId: getAccountStats
      x-api-path-slug: statsjson-get
      parameters:
      - in: query
        name: apiKey
        description: This API key is assigned to you by FullContact
      - in: query
        name: period
        description: You can define the month that you want to see usage stats for
          by using the period parameter
      responses:
        200:
          description: OK
      tags:
      - Statistics
  /email/disposable.json:
    get:
      summary: Lookup Email
      description: Lookup Email
      operationId: lookupEmail
      x-api-path-slug: emaildisposablejson-get
      parameters:
      - in: query
        name: apiKey
        description: This API key is assigned to you by FullContact
      - in: query
        name: email
        description: The email address that should be queried for being a disposable
          email address
      responses:
        200:
          description: OK
      tags:
      - Emails
  /company/lookup.json:
    get:
      summary: Get Company
      description: Get Company
      operationId: getCompany
      x-api-path-slug: companylookupjson-get
      parameters:
      - in: query
        name: apiKey
        description: This API key is assigned to you by FullContact
      - in: query
        name: callback
        description: If specified, the response will be wrapped as JSONP in a function
          call
      - in: query
        name: domain
        description: The domain of the company being looked up
      - in: query
        name: keyPeople
        description: ' If true, a list of Executive and VP level employees at this
          company will be returned under the keyPeople field'
      - in: query
        name: prettyPrint
        description: The prettyPrint parameter can be used to disable prettyprint
          formatting on the API response
      responses:
        200:
          description: OK
      tags:
      - Companies
  /icon:
    get:
      summary: Get Icons
      description: Get Icons
      operationId: getIcons
      x-api-path-slug: icon-get
      parameters:
      - in: query
        name: apiKey
        description: This API key is assigned to you by FullContact
      responses:
        200:
          description: OK
      tags:
      - Icons
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
---
swagger: "2.0"
x-collection-name: FullContact
x-complete: 0
info:
  title: FullContact Read Card
  description: Read Card
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
      x-api-path-slug: batch-json-get
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
      x-api-path-slug: stats-json-get
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
      x-api-path-slug: emaildisposable-json-get
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
      x-api-path-slug: companylookup-json-get
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
        description: If true, a list of Executive and VP level employees at this company
          will be returned under the keyPeople field
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
  /icon/{typeId}/{size}/{style}:
    get:
      summary: Get Icon
      description: Get Icon
      operationId: getIcon
      x-api-path-slug: icontypeidsizestyle-get
      parameters:
      - in: query
        name: apiKey
        description: This API key is assigned to you by FullContact
      - in: path
        name: size
        description: The size parameter allows you to specify the size of icon that
          you want
      - in: path
        name: style
        description: The style parameter allows you to pick from the available styles
          of the icons
      - in: path
        name: typeId
        description: The typeId is the name of the icon you want
      responses:
        200:
          description: OK
      tags:
      - Icons
  /v2/person.json:
    get:
      summary: ""
      description: Find out more about a person
      operationId: -v2-person
      x-api-path-slug: v2person-json-get
      parameters:
      - in: query
        name: email
        description: The email address you wish to query
      responses:
        200:
          description: OK
      tags:
      - People
  /cardReader:
    get:
      summary: Read Card
      description: Read Card
      operationId: readCard
      x-api-path-slug: cardreader-get
      parameters:
      - in: query
        name: apiKey
        description: This API key is assigned to you by FullContact
      - in: query
        name: casing
        description: Card Reader can alter the casing of certain fields in the final
          results
      - in: query
        name: Custom Params
        description: Card Reader has the ability to funnel your own custom params
          through requests
      - in: query
        name: format
        description: Used to specify response in json
      - in: body
        name: requestBody
        description: You can either send in the files as a multipart/form-data request
          or as a JSON object with BASE64 encoded images
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: returnedData
        description: A response can contain verified and unverified data, this parameter
          can be used to exclude unverified data from being returned in the response
      - in: query
        name: sandbox
        description: Card Reader Sandbox is a free, quick response mode for testing
          and development
      - in: query
        name: URID
        description: URID stands for Unique Request Identifier
      - in: query
        name: verified
        description: Used to specify the quality of transcription
      - in: query
        name: webhookUrl
        description: This is the URL that a request will be made to once the card
          has been processed
      responses:
        200:
          description: OK
      tags:
      - Card Reader
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
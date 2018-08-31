---
swagger: "2.0"
x-collection-name: FullContact
x-complete: 0
info:
  title: FullContact Get Account Stats
  description: Get Account Stats
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
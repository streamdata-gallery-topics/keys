---
swagger: "2.0"
x-collection-name: Logicbroker
x-complete: 0
info:
  title: Logic Broker CommerceAPI Returns the invoice with the specified key.
  version: 1.0.0
  description: Request rate limited to 10 requests per second with bursts up to 100
    requests.
host: stage.commerceapi.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/Acknowledgements/{LogicbrokerKey}/Status:
    get:
      summary: Retrieve acknowledgement status
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Acknowledgement_GetAckStatus
      x-api-path-slug: apiv1acknowledgementslogicbrokerkeystatus-get
      parameters:
      - in: path
        name: LogicbrokerKey
        description: The Logicbroker Key
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Acknowledgement
      - Status
  /api/v1/Acknowledgements/{LogicbrokerKey}/Status/{Status}:
    put:
      summary: Update acknowledgement status
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Acknowledgement_UpdateAckStatus
      x-api-path-slug: apiv1acknowledgementslogicbrokerkeystatusstatus-put
      parameters:
      - in: path
        name: LogicbrokerKey
        description: The Logicbroker Key
      - in: path
        name: Status
        description: The Status
      responses:
        200:
          description: OK
      tags:
      - Acknowledgement
      - Status
  /api/v1/Invoices/{LogicbrokerKey}:
    get:
      summary: Returns the invoice with the specified key.
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Invoice_GetInvoice
      x-api-path-slug: apiv1invoiceslogicbrokerkey-get
      parameters:
      - in: path
        name: LogicbrokerKey
        description: The logicbroker key to search for
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Invoice
      - Specified
      - Key
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
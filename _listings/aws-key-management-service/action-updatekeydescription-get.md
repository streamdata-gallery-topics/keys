---
swagger: "2.0"
info:
  title: AWS Key Management Service API Update Key Description
  version: 1.0.0
  description: Updates the description of a customer master key (CMK).
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=UpdateKeyDescription:
    get:
      summary: ' Update Key Description '
      description: Updates the description of a customer master key (CMK)
      operationId: updateKeyDescription
      parameters:
      - in: query
        name: Description
        description: New description for the CMK
        type: string
      - in: query
        name: KeyId
        description: A unique identifier for the CMK
        type: string
      responses:
        200:
          description: OK
      tags:
      - keys
definitions: []
x-collection-name: AWS Key Management Service
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
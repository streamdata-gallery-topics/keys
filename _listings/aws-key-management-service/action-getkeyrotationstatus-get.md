---
swagger: "2.0"
info:
  title: AWS Key Management Service API Get Key Rotation Status
  version: 1.0.0
  description: |-
    Retrieves a Boolean value that indicates whether key rotation is enabled for the
          specified key.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetKeyRotationStatus:
    get:
      summary: ' Get Key Rotation Status '
      description: |-
        Retrieves a Boolean value that indicates whether key rotation is enabled for the
              specified key
      operationId: getKeyRotationStatus
      parameters:
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key
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
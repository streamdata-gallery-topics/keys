---
swagger: "2.0"
info:
  title: Heroku Parameters User Keys Key
  description: Parameters user keys key.
  version: "1"
host: api.heroku.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/keys/{key}:
    parameters:
      summary: Parameters User Keys Key
      description: Parameters user keys key
      operationId: parametersUserKeysKey
      responses:
        200:
          description: OK
      tags:
      - parameters
      - user
      - keys
      - key
definitions: []
x-collection-name: Heroku
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
---
swagger: "2.0"
x-collection-name: Hewlett Packard Enterprise (HPE)
x-complete: 0
info:
  title: HPE OneSphere API Delete Tag Keys
  description: Delete a tag key and associated tags. It requires the **analyst** global
    role.
  termsOfService: http://www.hpe.com/onesphere
  contact:
    name: HPE OneSphere API team
    url: http://www.hpe.com/onesphere
  version: 1.0.0
host: deic02-hpe.hpeonesphere.com
basePath: /rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tag-keys:
    get:
      summary: Get Tag Keys
      description: Lists tag keys.
      operationId: ListTagKeys
      x-api-path-slug: tagkeys-get
      parameters:
      - in: query
        name: view
        description: 'Return related resources:  * `full` - include each tag-keys
          related `tags`'
      responses:
        200:
          description: OK
      tags:
      - Tag
      - Keys
    post:
      summary: Post Tag Keys
      description: Create a tag key. It requires the **analyst** global role.
      operationId: CreateTagKey
      x-api-path-slug: tagkeys-post
      parameters:
      - in: body
        name: name
        description: New tag key
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Tag
      - Keys
  /tag-keys/{id}:
    delete:
      summary: Delete Tag Keys
      description: Delete a tag key and associated tags. It requires the **analyst**
        global role.
      operationId: DeleteTagKey
      x-api-path-slug: tagkeysid-delete
      parameters:
      - in: path
        name: id
        description: ID of tag key to delete
      responses:
        200:
          description: OK
      tags:
      - Tag
      - Keys
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
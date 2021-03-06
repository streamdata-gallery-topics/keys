swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 1
info:
  title: plentymarkets REST-API
  description: the-plentymarkets-rest-api-expands-the-functionality-of-the-plentymarkets-cms-and-allows-access-to-resources-i-e--data-records-via-unique-uri-paths
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /export/{exportKey}:
    get:
      summary: Get Export Keys
      description: Get export keys.
      operationId: getExportExportkey
      x-api-path-slug: exportexportkey-get
      parameters:
      - in: path
        name: exportKey
      responses:
        200:
          description: OK
      tags:
      - Keys
  /export/{exportKey}/{token}:
    get:
      summary: Get Export Key
      description: Get export keys..
      operationId: getExportExportkeyToken
      x-api-path-slug: exportexportkeytoken-get
      parameters:
      - in: path
        name: exportKey
      - in: path
        name: token
      responses:
        200:
          description: OK
      tags:
      - Keys
  /rest/exports/format_keys:
    get:
      summary: Get format keys
      description: Shows all format keys registered by plugins in production state
      operationId: getRestExportsFormatKeys
      x-api-path-slug: restexportsformat-keys-get
      responses:
        200:
          description: OK
      tags:
      - Format
      - Keys
  /rest/exports/format_keys/{type}:
    get:
      summary: Get format keys
      description: Shows all format keys registered by plugins in production state
      operationId: getRestExportsFormatKeysType
      x-api-path-slug: restexportsformat-keystype-get
      parameters:
      - in: path
        name: type
      responses:
        200:
          description: OK
      tags:
      - Format
      - Keys
  /rest/accounting/locations/{locationId}/posting_key_configurations:
    get:
      summary: Get a posting key configuration of an accounting location
      description: Gets a posting key configuration of an accounting location. The
        ID of the accounting location has to be specified. The posting key configuration
        can contain up to 4 posting keys.
      operationId: getRestAccountingLocationsLocationAddingKeyConfigurations
      x-api-path-slug: restaccountinglocationslocationidposting-key-configurations-get
      parameters:
      - in: path
        name: locationId
      responses:
        200:
          description: OK
      tags:
      - Posting
      - Key
      - Configuration
      - Of
      - Accounting
      - Location
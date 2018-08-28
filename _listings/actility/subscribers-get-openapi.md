---
swagger: "2.0"
x-collection-name: Actility
x-complete: 0
info:
  title: ThingPark DX Core API Subscribers retrieval
  description: Retrieves a list of subscribers existing within authorized scopes.
  version: 1.0.0
host: dx-api.thingpark.com
basePath: /core/v141/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscribers:
    get:
      summary: Subscribers retrieval
      description: Retrieves a list of subscribers existing within authorized scopes.
      operationId: retrieves-a-list-of-subscribers-existing-within-authorized-scopes
      x-api-path-slug: subscribers-get
      parameters:
      - in: query
        name: applicationId
        description: Id of an application which has been subscribed by the searched
          subscribers
      - in: query
        name: contactEmail
        description: Contact email of the subscriber to search for
      - in: query
        name: subscriberId
        description: Id of the subscriber to search for
      responses:
        200:
          description: OK
      tags:
      - Subscribers
      - Retrieval
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
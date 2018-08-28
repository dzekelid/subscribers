---
swagger: "2.0"
x-collection-name: Actility
x-complete: 0
info:
  title: ThingPark DX Core API Subscriber creation
  description: Creates a new subscriber. If not fully specified, the subscriber name,
    contactEmail and organization attribute values are deduced from the primaryUser
    attribute values.
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
    post:
      summary: Subscriber creation
      description: Creates a new subscriber. If not fully specified, the subscriber
        name, contactEmail and organization attribute values are deduced from the
        primaryUser attribute values.
      operationId: creates-a-new-subscriber-if-not-fully-specified-the-subscriber-name-contactemail-and-organization-at
      x-api-path-slug: subscribers-post
      parameters:
      - in: body
        name: subscriber
        description: Contents of the subscriber to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Subscriber
      - Creation
  /subscribers/{subscriberRef}:
    get:
      summary: Subscriber retrieval
      description: Retrieves the subscriber corresponding to the provided subscriber
        ref, if that subscriber is within authorized scopes.
      operationId: retrieves-the-subscriber-corresponding-to-the-provided-subscriber-ref-if-that-subscriber-is-within-a
      x-api-path-slug: subscriberssubscriberref-get
      parameters:
      - in: path
        name: subscriberRef
        description: Ref of the subscriber to retrieve
      responses:
        200:
          description: OK
      tags:
      - Subscriber
      - Retrieval
    put:
      summary: Subscriber update
      description: Updates the subscriber corresponding to the provided subscriber
        ref, if that subscriber is within authorized scopes.
      operationId: updates-the-subscriber-corresponding-to-the-provided-subscriber-ref-if-that-subscriber-is-within-aut
      x-api-path-slug: subscriberssubscriberref-put
      parameters:
      - in: body
        name: subscriber
        description: Contents of the subscriber to update
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: subscriberRef
        description: Ref of the subscriber to update
      responses:
        200:
          description: OK
      tags:
      - Subscriber
      - Update
    delete:
      summary: Subscriber deletion
      description: Deletes the subscriber corresponding to the provided subscriber
        ref, if that subscriber is within authorized scopes.
      operationId: deletes-the-subscriber-corresponding-to-the-provided-subscriber-ref-if-that-subscriber-is-within-aut
      x-api-path-slug: subscriberssubscriberref-delete
      parameters:
      - in: query
        name: force
        description: If true, forces the deletion of all orders, devices and base
          stations attached to the subscriber, before deleting the subscriber
      - in: path
        name: subscriberRef
        description: Ref of the subscriber to delete
      responses:
        200:
          description: OK
      tags:
      - Subscriber
      - Deletion
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
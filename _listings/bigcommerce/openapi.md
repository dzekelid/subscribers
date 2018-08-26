---
swagger: "2.0"
x-collection-name: BigCommerce
x-complete: 1
info:
  title: BigCommerce API V3
  description: collection-of-requests-for-interacting-with-bigcommerces-v3-api
  version: 1.0.0
host: api.bigcommerce.com
basePath: /stores
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{store_hash}/v3/customers/subscribers:
    get:
      summary: Returns all newsletter subscribers
      description: Returns a paginated Subscribers collection.
      operationId: V3CustomersSubscribersByStoreHashGet
      x-api-path-slug: store-hashv3customerssubscribers-get
      parameters:
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Returns
      - ""
      - Newsletter
      - Subscribers
    delete:
      summary: Delete a group of subscribers by parameter
      description: ""
      operationId: V3CustomersSubscribersByStoreHashDelete
      x-api-path-slug: store-hashv3customerssubscribers-delete
      parameters:
      - in: query
        name: date_created
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Group
      - Of
      - Subscribers
      - By
      - Parameter
    post:
      summary: Create a new subscriber
      description: ""
      operationId: V3CustomersSubscribersByStoreHashPost
      x-api-path-slug: store-hashv3customerssubscribers-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - New
      - Subscriber
  /{store_hash}/v3/customers/subscribers/{id}:
    get:
      summary: Return a single subscriber by ID
      description: ""
      operationId: V3CustomersSubscribersByStoreHashAndIdGet
      x-api-path-slug: store-hashv3customerssubscribersid-get
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Return
      - Single
      - Subscriber
      - By
      - ID
    put:
      summary: Update a single subscriber
      description: ""
      operationId: V3CustomersSubscribersByStoreHashAndIdPut
      x-api-path-slug: store-hashv3customerssubscribersid-put
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Single
      - Subscriber
    delete:
      summary: Delete a single subscriber by ID
      description: ""
      operationId: V3CustomersSubscribersByStoreHashAndIdDelete
      x-api-path-slug: store-hashv3customerssubscribersid-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Single
      - Subscriber
      - By
      - ID
---
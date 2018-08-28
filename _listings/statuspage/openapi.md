swagger: "2.0"
x-collection-name: StatusPage
x-complete: 1
info:
  title: StatusPage.io
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /pages/[page_id]/subscribers/[subscriber_id].json:
    delete:
      summary: Delete a subscriber
      description: Delete a subscriber
      operationId: delete-a-subscriber
      x-api-path-slug: pagespage-idsubscriberssubscriber-id-json-delete
      responses:
        200:
          description: OK
      tags:
      - Subscribers
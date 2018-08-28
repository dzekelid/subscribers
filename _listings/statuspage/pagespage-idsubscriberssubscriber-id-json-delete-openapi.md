---
swagger: "2.0"
x-collection-name: StatusPage
x-complete: 0
info:
  title: StatusPage.io Delete a subscriber
  version: 1.0.0
  description: Delete a subscriber
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
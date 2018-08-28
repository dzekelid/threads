---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Delete Notifications Threads  Subscription
  description: Delete a Thread Subscription.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /notifications/threads/{id}:
    get:
      summary: Get Notifications Threads
      description: View a single thread.
      operationId: view-a-single-thread
      x-api-path-slug: notificationsthreadsid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
        description: Id of thread
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Threads
    patch:
      summary: Patch Notifications Threads
      description: Mark a thread as read
      operationId: mark-a-thread-as-read
      x-api-path-slug: notificationsthreadsid-patch
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
        description: Id of thread
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Threads
  /notifications/threads/{id}/subscription:
    delete:
      summary: Delete Notifications Threads  Subscription
      description: Delete a Thread Subscription.
      operationId: delete-a-thread-subscription
      x-api-path-slug: notificationsthreadsidsubscription-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
        description: Id of thread
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Threads
      - ""
      - Subscription
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
---
swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 0
info:
  title: Microsoft Graph List Threads
  description: List threads Get all the threads of a group.
  version: 1.0.0
host: graph.microsoft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{id}/threads:
    get:
      summary: List Threads
      description: List threads Get all the threads of a group.
      operationId: ListThreads
      x-api-path-slug: groupsidthreads-get
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
      - in: path
        name: id
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Threads
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
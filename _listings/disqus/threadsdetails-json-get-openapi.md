---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Threads Details
  description: Threads Details
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /threads/close.json:
    post:
      summary: Threads Close
      description: Threads Close
      operationId: threads-close
      x-api-path-slug: threadsclose-json-post
      parameters:
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You must be a moderator on the selected
          thread&#39;s forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/create.json:
    post:
      summary: Threads Create
      description: Threads Create
      operationId: threads-create
      x-api-path-slug: threadscreate-json-post
      parameters:
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: date
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: identifier
        description: Defaults to null                         Maximum length of 300
        type: string
      - in: query
        name: message
        description: Defaults to null
        type: string
      - in: query
        name: slug
        description: Defaults to null                         Alpha-numeric slug Maximum
          length of 200
        type: string
      - in: query
        name: title
        type: string
      - in: query
        name: url
        description: Defaults to null                         URL (defined by RFC
          3986) Maximum length of 500
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/details.json:
    get:
      summary: Threads Details
      description: Threads Details
      operationId: threads-details
      x-api-path-slug: threadsdetails-json-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: topics'
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID You may pass us the &#39;ident&#39; or
          &#39;link&#39; query types instead of an ID by including &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
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
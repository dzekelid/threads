---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Threads ListPopular
  description: Threads ListPopular
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
  /threads/list.json:
    get:
      summary: Threads List
      description: Threads List
      operationId: threads-list
      x-api-path-slug: threadslist-json-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: topics'
        type: string
      - in: query
        name: author
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: include
        description: 'Defaults to [  open,  closed]                         Choices:
          open, closed, killed'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID You may pass us the &#39;ident&#39; query type instead of an ID by including
          &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/listHot.json:
    get:
      summary: Threads ListHot
      description: Threads ListHot
      operationId: threads-listhot
      x-api-path-slug: threadslisthot-json-get
      parameters:
      - in: query
        name: author
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: include
        description: 'Defaults to [  open,  closed]                         Choices:
          open, closed, killed'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/listPopular.json:
    get:
      summary: Threads ListPopular
      description: Threads ListPopular
      operationId: threads-listpopular
      x-api-path-slug: threadslistpopular-json-get
      parameters:
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: interval
        description: 'Defaults to 7d                         Choices: 1h, 6h, 12h,
          1d, 3d, 7d, 30d, 90d'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: with_top_post
        description: Defaults to false
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
x-streamrank:
  polling_total_time_average: "0.34"
  polling_size_download_average: "25351.58"
  streaming_total_time_average: "0.18"
  streaming_size_download_average: "12685.63"
  change_yes: "258"
  change_no: "935"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "22"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---
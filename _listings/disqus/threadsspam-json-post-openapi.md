---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Threads Spam
  description: Threads Spam
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
  /threads/listPosts.json:
    get:
      summary: Threads ListPosts
      description: Threads ListPosts
      operationId: threads-listposts
      x-api-path-slug: threadslistposts-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: filters
        description: 'Defaults to []                         Valid values are: 1:
          Is_Anonymous 2: Has_Link 3: Has_Low_Rep_Author 4: Has_Bad_Word 5: Is_Flagged
          6: No_Issue 7: Is_Toxic'
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: include
        description: 'Defaults to [  approved]                         Choices: unapproved,
          approved, spam, deleted, flagged, highlighted'
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
        name: query
        description: Defaults to null
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
        description: Looks up a thread by ID You may pass us the &#39;ident&#39; or
          &#39;link&#39; query types instead of an ID by including &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/listUsersVotedThread.json:
    get:
      summary: Threads ListUsersVotedThread
      description: Threads ListUsersVotedThread
      operationId: threads-listusersvotedthread
      x-api-path-slug: threadslistusersvotedthread-json-get
      parameters:
      - in: query
        name: limit
        description: Defaults to 10                         Maximum value of 100
        type: string
      - in: query
        name: prioritize_followed
        description: Defaults to true                         Prioritize followed
          users who voted on this thread (must be authenticated)
        type: string
      - in: query
        name: thread
        description: Looks up a thread by ID
        type: string
      - in: query
        name: vote
        description: 'Defaults to 1                         Choices: -1, 0, 1'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/open.json:
    post:
      summary: Threads Open
      description: Threads Open
      operationId: threads-open
      x-api-path-slug: threadsopen-json-post
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
  /threads/remove.json:
    post:
      summary: Threads Remove
      description: Threads Remove
      operationId: threads-remove
      x-api-path-slug: threadsremove-json-post
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
  /threads/restore.json:
    post:
      summary: Threads Restore
      description: Threads Restore
      operationId: threads-restore
      x-api-path-slug: threadsrestore-json-post
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
  /threads/set.json:
    get:
      summary: Threads Set
      description: Threads Set
      operationId: threads-set
      x-api-path-slug: threadsset-json-get
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
        description: Looks up a thread by ID You may pass us the &#39;ident&#39; query
          type instead of an ID by including &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Threads
  /threads/spam.json:
    post:
      summary: Threads Spam
      description: Threads Spam
      operationId: threads-spam
      x-api-path-slug: threadsspam-json-post
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
      - Spam
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
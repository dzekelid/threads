---
swagger: "2.0"
x-collection-name: Context.IO
x-complete: 0
info:
  title: Context.IO Get Accounts Threads
  description: Lists threads on an account.
  version: 1.0.0
host: api.context.io
basePath: /2.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts/{id}/contacts/{email}/threads:
    get:
      summary: Get Accounts Contacts Email Threads
      description: Lists threads where a contact is present. Returns the latest email
        threads exchanged with one or more email addresses. By "exchanged with Mr.
        X" we mean any email received from Mr. X, sent to Mr. X or sent by anyone
        to both Mr. X and the mailbox owner.
      operationId: listAccountContactThreads_
      x-api-path-slug: accountsidcontactsemailthreads-get
      parameters:
      - in: path
        name: email
        description: Email address of a contact
      - in: path
        name: id
        description: Unique id of an account accessible through your API key
      - in: query
        name: limit
        description: The maximum number of results to return
      - in: query
        name: offset
        description: Start the list at this offset (zero-based)
      responses:
        200:
          description: OK
      tags:
      - Accounts
      - Contacts
      - Email
      - Threads
  /accounts/{id}/threads:
    get:
      summary: Get Accounts Threads
      description: Lists threads on an account.
      operationId: listAccountThreads_
      x-api-path-slug: accountsidthreads-get
      parameters:
      - in: query
        name: active_after
        description: Get threads with at least one message dated after this timestamp
      - in: query
        name: active_before
        description: Get threads with at least one message dated before this timestamp
      - in: query
        name: bcc
        description: Get threads with at least one message having this email address
          BCCed
      - in: query
        name: cc
        description: Get threads with at least one message having this email address
          CCed
      - in: query
        name: email
        description: Email address of the contact for whom you want the latest threads
      - in: query
        name: folder
        description: Filter threads by the folder (or Gmail label)
      - in: query
        name: from
        description: Get threads with at least one message sent from this email address
      - in: path
        name: id
        description: Unique id of an account accessible through your API key
      - in: query
        name: indexed_after
        description: Get threads with at least one message indexed after this timestamp
      - in: query
        name: indexed_before
        description: Get threads with at least one message indexed before this timestamp
      - in: query
        name: limit
        description: The maximum number of results to return
      - in: query
        name: offset
        description: Start the list at this offset (zero-based)
      - in: query
        name: started_after
        description: Get threads whose first message is dated after this timestamp
      - in: query
        name: started_before
        description: Get threads whose first message is dated before this timestamp
      - in: query
        name: subject
        description: Get threads with messages whose subject matches this search string
      - in: query
        name: to
        description: Get threads with at least one message sent to this email address
      responses:
        200:
          description: OK
      tags:
      - Accounts
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
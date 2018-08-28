swagger: "2.0"
x-collection-name: Context.IO
x-complete: 1
info:
  title: Context.IO
  description: context-io-is-the-missing-email-api-that-makes-it-easy-and-fast-to-integrate-your-users-email-data-in-your-application-
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
  /accounts/{id}/threads/{thread_id}:
    get:
      summary: Get Accounts Threads Thread
      description: |-
        Returns files, contacts and messages on a given thread. The purpose is to allow Gmail extensions to easily retrieve data when users's load a conversation in the Gmail UI. Hence, threads are identified by the value of their Gmail thread prefixed with "gm-".
        For example, if the URL of a conversation in the Gmail UI is https://mail.google.com/mail/u/0/#mbox/13119ab37f00b826, you would obtain the details about this thread by calling:
        GET https://api.context.io/2.0/accounts/<accountId>/threads/gm-13119ab37f00b826

        What about threads on non-Gmail mailboxes?
        You can retrieve thread information for any message using the Thread resource of that message.
      operationId: getAccountThread_
      x-api-path-slug: accountsidthreadsthread-id-get
      parameters:
      - in: path
        name: id
        description: Unique id of an account accessible through your API key
      - in: path
        name: thread_id
        description: A gmail_thread_id prefixed with gm-
      responses:
        200:
          description: OK
      tags:
      - Accounts
      - Threads
      - Thread
  /accounts/{id}/messages/{message_id}/thread:
    get:
      summary: Get Accounts Messages Message Thread
      description: Gets information about all messages of the thread a given message
        is in. This returns an array with the same structure as getting information
        on a single message for every message in the thread.
      operationId: getAccountMessageThread_
      x-api-path-slug: accountsidmessagesmessage-idthread-get
      parameters:
      - in: path
        name: id
        description: Unique id of an account accessible through your API key
      - in: path
        name: message_id
        description: Unique id of a message
      responses:
        200:
          description: OK
      tags:
      - Accounts
      - Messages
      - Message
      - Thread
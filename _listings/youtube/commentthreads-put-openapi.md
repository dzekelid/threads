---
swagger: "2.0"
x-collection-name: YouTube
x-complete: 0
info:
  title: Youtube Put Comment Threads
  description: Modifies the top-level comment in a comment thread.
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: 1.0.0
host: www.googleapis.com
basePath: /youtube/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /commentThreads:
    get:
      summary: Get Comment Threads
      description: Returns a list of comment threads that match the API request parameters.
      operationId: getCommentthreads
      x-api-path-slug: commentthreads-get
      parameters:
      - in: query
        name: allThreadsRelatedToChannelId
        description: The allThreadsRelatedToChannelId parameter instructs the API
          to return all comment threads associated with the specified channel
      - in: query
        name: channelId
        description: The channelId parameter instructs the API to return comment threads
          containing comments about the specified channel
      - in: query
        name: id
        description: The id parameter specifies a comma-separated list of comment
          thread IDs for the resources that should be retrieved
      - in: query
        name: maxResults
        description: The maxResults parameter specifies the maximum number of items
          that should be returned in the result set
      - in: query
        name: moderationStatus
        description: Set this parameter to limit the returned comment threads to a
          particular moderation state
      - in: query
        name: order
        description: The order parameter specifies the order in which the API response
          should list comment threads
      - in: query
        name: pageToken
        description: The pageToken parameter identifies a specific page in the result
          set that should be returned
      - in: query
        name: part
        description: The part parameter specifies a comma-separated list of one or
          more commentThread resource properties that the API response will include
      - in: query
        name: searchTerms
        description: The searchTerms parameter instructs the API to limit the API
          response to only contain comments that contain the specified search terms
      - in: query
        name: textFormat
        description: Set this parameters value to html or plainText to instruct the
          API to return the comments left by users in html formatted or in plain text
      - in: query
        name: videoId
        description: The videoId parameter instructs the API to return comment threads
          associated with the specified video ID
      responses:
        200:
          description: OK
      tags:
      - Commentthreads
    post:
      summary: Add Comment Threads
      description: Creates a new top-level comment. To add a reply to an existing
        comment, use the comments.insert method instead.
      operationId: postCommentthreads
      x-api-path-slug: commentthreads-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: part
        description: The part parameter identifies the properties that the API response
          will include
      responses:
        200:
          description: OK
      tags:
      - Commentthreads
    put:
      summary: Put Comment Threads
      description: Modifies the top-level comment in a comment thread.
      operationId: putCommentthreads
      x-api-path-slug: commentthreads-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: part
        description: The part parameter specifies a comma-separated list of commentThread
          resource properties that the API response will include
      responses:
        200:
          description: OK
      tags:
      - Commentthreads
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
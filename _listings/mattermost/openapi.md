swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost
  version: 1.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /posts/{post_id}/thread:
    get:
      summary: Get a thread
      description: |-
        Get a post and the rest of the posts in the same thread.
        ##### Permissions
        Must have `read_channel` permission for the channel the post is in or if the channel is public, have the `read_public_channels` permission for the team.
      operationId: get-a-post-and-the-rest-of-the-posts-in-the-same-thread-permissionsmust-have-read-channel-permission
      x-api-path-slug: postspost-idthread-get
      parameters:
      - in: path
        name: post_id
        description: ID of a post in the thread
      responses:
        200:
          description: OK
      tags:
      - Thread
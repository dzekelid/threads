{
  "info": {
    "name": "Youtube Get Comment Threads",
    "_postman_id": "244e88f4-c03a-4e35-a433-ffa9705889cf",
    "description": "Returns a list of comment threads that match the API request parameters.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "commentthreads",
      "item": [
        {
          "id": "0b68ca88-e947-4c7e-a5bc-184ae40729ea",
          "name": "getCommentthreads",
          "request": {
            "url": "http://www.googleapis.com/youtube/v1/commentThreads?allThreadsRelatedToChannelId=%7B%7D&channelId=%7B%7D&id=%7B%7D&maxResults=%7B%7D&moderationStatus=%7B%7D&order=%7B%7D&pageToken=%7B%7D&part=%7B%7D&searchTerms=%7B%7D&textFormat=%7B%7D&videoId=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of comment threads that match the API request parameters"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b6f8091e-a9f9-406f-834a-fd0e2ed08661"
            }
          ]
        }
      ]
    }
  ]
}
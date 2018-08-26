{
  "info": {
    "name": "HERE Venue Maps Venue Clusters within a Bounding Box",
    "_postman_id": "9fc5ca7a-e829-4e4c-b3e7-5a32a7c6665b",
    "description": "*Request an overview of the number venues across a large area*\n\nA bounding box is specified using the `bbox` parameter in the request URL.\n\n\n\n* **bbox**  `bbox`\n \\- A type of spatial filter. A bounding box specifies the top-right and bottom left corners of an area to search.    e.g. `52.515,13.377;52.134,13.978`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Venue",
      "item": [
        {
          "id": "46c2bf3b-e00f-496b-ba54-9afbd7bb3b31",
          "name": "V1Get3",
          "request": {
            "url": "http://signature.venue.maps.cit.api.here.com/venues/signature/v1?app_code=%7B%7D&app_id=%7B%7D&bbox=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request an overview of the number venues across a large area*\n\nA bounding box is specified using the `bbox` parameter in the request URL.\n\n\n\n* **bbox**  `bbox`\n \\- A type of spatial filter. A bounding box specifies the top-right and bottom left corners of an area to search.    e.g. `52.515,13.377;52.134,13.978`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "39e53fe3-7062-4ff6-b4ed-18d2c940c437"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "HERE Map Tile API Point of Interest Categories",
    "_postman_id": "5423f704-f42d-41d7-a2b7-d1a53f3304e7",
    "description": "*Request point of interest category information*\n\nTo make a request for point-of-interest information, use `meta/pois` in the path of the request URL.\n  \n\n\n\n* **output**  `enum`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n Valid values are : `json`, `text`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request..  \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Point",
      "item": [
        {
          "id": "7fd6cc1f-9a2a-45c9-b82b-8f6502815642",
          "name": "MetaPoisGet",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/meta/pois?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D",
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
            "description": "*Request point of interest category information*\n\nTo make a request for point-of-interest information, use `meta/pois` in the path of the request URL.\n  \n\n\n\n* **output**  `enum`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n Valid values are : `json`, `text`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request..  \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fa14528d-1023-4a6d-9d42-54c36c7dc1b2"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "HERE Map Tile API Copyright Information",
    "_postman_id": "a211425c-ae25-49c7-9c4c-13307b96b0d6",
    "description": "*Request map tile copyright information*\n\nTo make a request for copyright information, use the `copyright` parameter in the path of the request URL.\n  \n  Note that the client-side process formatting the JSON response may take some time in older browsers.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Copyright",
      "item": [
        {
          "id": "91459023-48fd-4b1a-8dc2-b565d14c9927",
          "name": "CopyrightNewestGet",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/copyright/newest?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request map tile copyright information*\n\nTo make a request for copyright information, use the `copyright` parameter in the path of the request URL.\n  \n  Note that the client-side process formatting the JSON response may take some time in older browsers.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0d79919e-c419-4501-b83c-7310dd098a08"
            }
          ]
        }
      ]
    }
  ]
}
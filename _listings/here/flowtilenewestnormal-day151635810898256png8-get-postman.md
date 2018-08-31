{
  "info": {
    "name": "HERE Traffic API Transparent Traffic Map",
    "_postman_id": "3e947dc3-69e9-4e7a-8f1f-97a428572cd0",
    "description": "*Request a transparent tile with traffic flow information*\n\nTo obtain a transparent map tile displaying traffic flow, use the `flowtile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Transparent",
      "item": [
        {
          "id": "e5ff2134-eea3-4e58-89f1-01f11ec03ba8",
          "name": "FlowtileNewestNormalDay151635810898256Png8Get",
          "request": {
            "url": "http://tiles.traffic.cit.api.here.com/traffic/6.0/tiles/8/133/86/256/flowtile/newest/normal.day/15/16358/10898/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a transparent tile with traffic flow information*\n\nTo obtain a transparent map tile displaying traffic flow, use the `flowtile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5b1115d-e4b5-4e6a-9b56-457c18073710"
            }
          ]
        },
        {
          "id": "edb69b2a-43eb-4f3a-90a6-17f7a712437a",
          "name": "Png32Get",
          "request": {
            "url": "http://tiles.traffic.cit.api.here.com/traffic/6.0/tiles/8/133/86/256/png32?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a transparent tile with traffic flow information*\n\nSupports custom coloring, functional class filters, DLR rendering, sub-segment traffic rendering.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60880b05-b3c5-4c40-96ec-ace3d4d65288"
            }
          ]
        }
      ]
    },
    {
      "name": "Traffic",
      "item": [
        {
          "id": "a8f2dd35-fc6b-496c-975e-e1e2201b8d6d",
          "name": "TraffictileNewestNormalDay151635810898256Png8Get",
          "request": {
            "url": "http://tiles.traffic.cit.api.here.com/traffic/6.0/tiles/8/133/86/256/traffictile/newest/normal.day/15/16358/10898/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a map tile with traffic flow information*\n\nTo obtain a traffic map tile, use the  `traffictile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8352d6c7-f230-492d-b723-ab1b38fdabbe"
            }
          ]
        }
      ]
    }
  ]
}
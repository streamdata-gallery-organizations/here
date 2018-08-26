{
  "info": {
    "name": "HERE Traffic API Transparent Traffic Map via TDA (to be deprecated)",
    "_postman_id": "337fe40a-ec08-4561-b5a9-0738d28b7358",
    "description": "*Request a transparent tile with traffic flow information*\n\nSupports custom coloring, functional class filters, DLR rendering, sub-segment traffic rendering.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Transparent",
      "item": [
        {
          "id": "c1ba4eb4-2281-4a97-8853-976bf6d942f0",
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
              "id": "85e7469d-bb19-4eb7-865b-31559467bf82"
            }
          ]
        },
        {
          "id": "d5677d32-db87-4e86-a2f1-965280d88afe",
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
              "id": "e35241a0-081f-4f33-a3c0-514fac431793"
            }
          ]
        }
      ]
    },
    {
      "name": "Traffic",
      "item": [
        {
          "id": "37ceb85e-8bc0-460b-a029-c795f800581f",
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
              "id": "32fa95e9-7a95-4c0e-ae56-5a5caa58e450"
            }
          ]
        }
      ]
    }
  ]
}
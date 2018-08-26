{
  "info": {
    "name": "HERE Traffic API Traffic Map",
    "_postman_id": "25e511f1-d3c2-4dc7-84f7-9929e858b019",
    "description": "*Request a map tile with traffic flow information*\n\nTo obtain a traffic map tile, use the  `traffictile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Transparent",
      "item": [
        {
          "id": "837deaac-9a54-4a5a-851a-9ac4d8c70cef",
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
              "id": "7a6c791c-9f91-4dd6-82fb-9ea1e3fdfaa8"
            }
          ]
        },
        {
          "id": "d6629789-64f3-4723-8132-10638ea7ab22",
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
              "id": "f23731d4-75ad-4fce-bfd4-29ca8de55449"
            }
          ]
        }
      ]
    },
    {
      "name": "Traffic",
      "item": [
        {
          "id": "1948a68b-2f64-4cf1-b0ad-38da5d22572a",
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
              "id": "4b8b3ca8-ea8c-4894-8960-fb7bdfe4a12d"
            }
          ]
        }
      ]
    }
  ]
}
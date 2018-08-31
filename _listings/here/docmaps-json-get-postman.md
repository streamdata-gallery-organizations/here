{
  "info": {
    "name": "HERE Route Match Extension API Map Data Availability and Freshness",
    "_postman_id": "44154f86-8d7a-4450-8072-dff9368bd5a4",
    "description": "*Request the release date and area covered by each available map region*\n\nTo make a request for release date information, use the `maps.json` endpoint.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Available",
      "item": [
        {
          "id": "b1146cf5-ca39-4349-92bd-1b6fe9d733a8",
          "name": "DocLayersJsonGet",
          "request": {
            "url": "http://pde.cit.api.here.com/1/doc/layers.json?app_code=%7B%7D&app_id=%7B%7D&region=%7B%7D&release=%7B%7D",
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
            "description": "*Request which data layers can be accessed within a specified map region and release*\n\nTo make a request for data layer availability information, use the `layers.json` endpoint, supplying the `release` and `region` parameters.\n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cc4bc6df-e27e-46b1-b5d1-56f05d1b1a5a"
            }
          ]
        },
        {
          "id": "8086a7b2-bec5-444e-a568-13c3f1e8c464",
          "name": "DocLayerJsonGet",
          "request": {
            "url": "http://pde.cit.api.here.com/1/doc/layer.json?app_code=%7B%7D&app_id=%7B%7D&layer=%7B%7D&region=%7B%7D&release=%7B%7D",
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
            "description": "*Request which attributes are available within a specified map data layer*\n\nTo make a request for map data layer information, use the `layer``.json` endpoint, supplying the `release`, `layer` and `region` parameters.\n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **layer**  `text`\n \\- Thematic layer\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d46b09e0-08df-4102-b732-2a6dd9a135d5"
            }
          ]
        }
      ]
    },
    {
      "name": "Map",
      "item": [
        {
          "id": "f77a27ef-ad06-4385-8149-3d5c4226f9d4",
          "name": "DocMapsJsonGet",
          "request": {
            "url": "http://pde.cit.api.here.com/1/doc/maps.json?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request the release date and area covered by each available map region*\n\nTo make a request for release date information, use the `maps.json` endpoint.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5429bbc9-c85a-4662-86db-d6da3030785b"
            }
          ]
        }
      ]
    }
  ]
}
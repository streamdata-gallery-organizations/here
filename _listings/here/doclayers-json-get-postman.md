{
  "info": {
    "name": "HERE Route Match Extension API Available Map Data Layers",
    "_postman_id": "d9eada1c-8151-4728-b886-c6ae473090b0",
    "description": "*Request which data layers can be accessed within a specified map region and release*\n\nTo make a request for data layer availability information, use the `layers.json` endpoint, supplying the `release` and `region` parameters.\n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Available",
      "item": [
        {
          "id": "872b6080-e6d7-42a0-ad9a-f215ef7016f8",
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
              "id": "dfe9f68c-97e5-4d2a-a459-c20c221b9866"
            }
          ]
        },
        {
          "id": "988aeabc-e858-443c-9cd9-0e8524499cc3",
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
              "id": "c56ef69e-b729-4d0c-8ece-51d3e0bf4865"
            }
          ]
        }
      ]
    },
    {
      "name": "Map",
      "item": [
        {
          "id": "49751275-50f2-45f4-8017-398376a78dd6",
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
              "id": "1371b60d-986f-437b-adc7-99de4887d449"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "HERE Route Match Extension API Platform Data",
    "_postman_id": "e9ff2711-a289-4d69-91c6-21748ca2c612",
    "description": "*Request data from a specific data layer about a specified location*\n\nTo request data  from a specified data layer, use the t`ile.json` endpoint, and include the `region`, `release` and `layer` parameters. The area covered is specified by the `level`, `tilex` and `tiley` parameters\n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **layer**  `text`\n \\- Thematic layer\n\n* **level**  `text`\n \\- Specifies the size of the requested tile\n\n* **tilex**  `text`\n \\- Specifies the tile number in West-East direction. This depends on the level.\n\n* **tiley**  `text`\n \\- Specifies the tile number in South-North direction. This depends on the level.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Platform",
      "item": [
        {
          "id": "29a5cd28-d1ab-425f-8f00-eac13372c05b",
          "name": "StaticJsonGet",
          "request": {
            "url": "http://pde.cit.api.here.com/1/static.json?app_code=%7B%7D&app_id=%7B%7D&content=%7B%7D&region=%7B%7D&release=%7B%7D",
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
            "description": "*Request enumerated content from a static data table*\n\nTo request static data use the static.json endpoint and provide the name of the data table using the `content` parameter\n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **content**  `text`\n \\- The name of the static content table requested\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fdab1322-655c-4c6f-9821-e6bca4ef44ed"
            }
          ]
        },
        {
          "id": "06a21ddc-06ec-4ec3-95ce-c003c40ef085",
          "name": "TileJsonGet",
          "request": {
            "url": "http://pde.cit.api.here.com/1/tile.json?app_code=%7B%7D&app_id=%7B%7D&layer=%7B%7D&level=%7B%7D&region=%7B%7D&release=%7B%7D&tilex=%7B%7D&tiley=%7B%7D",
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
            "description": "*Request data from a specific data layer about a specified location*\n\nTo request data  from a specified data layer, use the t`ile.json` endpoint, and include the `region`, `release` and `layer` parameters. The area covered is specified by the `level`, `tilex` and `tiley` parameters\n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **layer**  `text`\n \\- Thematic layer\n\n* **level**  `text`\n \\- Specifies the size of the requested tile\n\n* **tilex**  `text`\n \\- Specifies the tile number in West-East direction. This depends on the level.\n\n* **tiley**  `text`\n \\- Specifies the tile number in South-North direction. This depends on the level.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "339a7a15-f2d1-447a-958c-3b3ebeb89026"
            }
          ]
        }
      ]
    },
    {
      "name": "Available",
      "item": [
        {
          "id": "52bcf98f-743d-4383-a9b1-c4fbdcca169c",
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
              "id": "fc5b26e2-5a0c-4ae5-a10d-f25e9da03177"
            }
          ]
        }
      ]
    }
  ]
}
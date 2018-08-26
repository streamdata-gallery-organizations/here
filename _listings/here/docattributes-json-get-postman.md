{
  "info": {
    "name": "HERE Route Match Extension API Available Attributes",
    "_postman_id": "d444227a-022e-4631-bde8-7388347c82f1",
    "description": "*Request which map data layers contain which attributes*\n\nTo make a request for map data layer information, use the `attributes``.json` endpoint, supplying the `release` and `region` parameters.\n  \n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Available",
      "item": [
        {
          "id": "a791bc51-48ee-4261-9544-9b1c16400e0c",
          "name": "DocAttributesJsonGet",
          "request": {
            "url": "http://pde.cit.api.here.com/1/doc/attributes.json?app_code=%7B%7D&app_id=%7B%7D&region=%7B%7D&release=%7B%7D",
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
            "description": "*Request which map data layers contain which attributes*\n\nTo make a request for map data layer information, use the `attributes``.json` endpoint, supplying the `release` and `region` parameters.\n  \n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90173e7a-0dfa-4855-a99a-5f951e00b059"
            }
          ]
        }
      ]
    }
  ]
}
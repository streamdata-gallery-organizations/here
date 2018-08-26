{
  "info": {
    "name": "HERE Route Match Extension API Platform Static Data",
    "_postman_id": "3e5ef9e7-3818-4d21-91bb-ba8b467498fe",
    "description": "*Request enumerated content from a static data table*\n\nTo request static data use the static.json endpoint and provide the name of the data table using the `content` parameter\n\n\n\n* **region**  `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **content**  `text`\n \\- The name of the static content table requested\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Platform",
      "item": [
        {
          "id": "a10e078d-87b9-4fae-87ef-ab8948d3c04e",
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
              "id": "5454ab0c-b5b6-4517-9d08-e35f1fd4c008"
            }
          ]
        }
      ]
    }
  ]
}
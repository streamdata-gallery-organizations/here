{
  "info": {
    "name": "HERE Custom Location Extension API Find the Five Nearest Locations",
    "_postman_id": "44901af8-5dbc-487e-b67e-cd93140cfa90",
    "description": "*Request a list of user-defined locations within a circle around a fixed point*\n\nThe search uses the `proximity` endpoint. The definition of the location and limit of the search is specified using  `coord` and `radius` parameters, and the number of results returned limited by adding the `limit` parameter to the request URL.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **coord**  `latlng`\n \\- Center of the proximity search\n\n* **radius**  `number`\n \\- width of the search corridor\n\n* **limit**  `number`\n \\- The limit of the number of items contained in the response.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Find",
      "item": [
        {
          "id": "582aa69c-8af3-4fd5-9ba8-e35a9fd8b0bb",
          "name": "BboxGet2",
          "request": {
            "url": "http://customlocation.cit.api.here.com/v1/search/bbox?app_code=%7B%7D&app_id=%7B%7D&bbox=%7B%7D&layerId=%7B%7D",
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
            "description": "*Request a list of user-defined locations within a defined area*\n\nThe request uses the `bbox` endpoint, and the bounding box is specified by adding the `bbox` parameter to the request URL.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **bbox**  `bbox`\n \\- Restricts results to be found within this bounding box\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3b60d324-cadb-4721-9038-c9ded9c9a38a"
            }
          ]
        },
        {
          "id": "1e019243-a565-41ea-b83f-3c7effd14cd1",
          "name": "ProximityGet2",
          "request": {
            "url": "http://customlocation.cit.api.here.com/v1/search/proximity?app_code=%7B%7D&app_id=%7B%7D&coord=%7B%7D&layerId=%7B%7D&limit=%7B%7D&radius=%7B%7D",
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
            "description": "*Request a list of user-defined locations within a circle around a fixed point*\n\nThe search uses the `proximity` endpoint. The definition of the location and limit of the search is specified using  `coord` and `radius` parameters, and the number of results returned limited by adding the `limit` parameter to the request URL.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **coord**  `latlng`\n \\- Center of the proximity search\n\n* **radius**  `number`\n \\- width of the search corridor\n\n* **limit**  `number`\n \\- The limit of the number of items contained in the response.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2a7d15e9-1047-4a6a-bfc3-bdd5fd386ba9"
            }
          ]
        }
      ]
    }
  ]
}
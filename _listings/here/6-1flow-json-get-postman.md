{
  "info": {
    "name": "HERE Traffic API Flow using Proximity returning Additional Attributes",
    "_postman_id": "bfa0eeb7-e5c4-4cb6-8b46-b2de81a3e5d8",
    "description": "*Request traffic flow information using proximity, returning shape and functional class*\n\nThe request is made through combining the `prox` parameter and the `responseattributes` in the request URL. The server also supports an XML response.\n\n\n\n* **prox**  `prox`\n \\- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`\n\n* **responseattributes**  `multi-enum`\n \\- A list indicating optional information to be included in the traffic flow data response\n\n Valid values are : `fc` - functionalClass, `sh` - shape\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Flow",
      "item": [
        {
          "id": "cc4917cc-858d-4faa-914c-089a61048892",
          "name": "61FlowJsonGet7",
          "request": {
            "url": "http://tiles.traffic.cit.api.here.com/traffic/6.0/tiles/8/133/86/256/6.1/flow.json?app_code=%7B%7D&app_id=%7B%7D&prox=%7B%7D&responseattributes=%7B%7D",
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
            "description": "*Request traffic flow information using proximity, returning shape and functional class*\n\nThe request is made through combining the `prox` parameter and the `responseattributes` in the request URL. The server also supports an XML response.\n\n\n\n* **prox**  `prox`\n \\- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`\n\n* **responseattributes**  `multi-enum`\n \\- A list indicating optional information to be included in the traffic flow data response\n\n Valid values are : `fc` - functionalClass, `sh` - shape\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0085fd3c-e1e3-44aa-bac6-501273ff5a70"
            }
          ]
        }
      ]
    }
  ]
}
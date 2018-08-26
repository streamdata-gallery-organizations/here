{
  "info": {
    "name": "HERE Routing API Avoid motorways",
    "_postman_id": "a82a457e-be22-4f8a-9371-6b2ad7889933",
    "description": "*Request a route preferring or avoiding specific types of road*\n\nRouting preferences can be added by extending the `mode` parameter of the request URL by adding a semi-colon delimited list of route link flags. In this case the addition of `motorway:-3` to the `mode` parameter indicates a strict exclusion of motorways. Consult the Routing API Reference for a full description of `mode` parameter and different feature weights.\n\n\n\n* **waypoint0**  `latlng`\n \\- Start point of the route.    e.g. `52.515,13.377`\n\n* **waypoint1**  `latlng`\n \\- Second point through which the route must pass.    e.g. `52.6172,13.3833`\n\n* **mode**  `text`\n \\- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Avoid",
      "item": [
        {
          "id": "c66c6079-59dd-45c5-b710-42b124366d5c",
          "name": "CalculaterouteJsonGet22",
          "request": {
            "url": "http://route.cit.api.here.com/routing/7.2/calculateroute.json?app_code=%7B%7D&app_id=%7B%7D&mode=%7B%7D&waypoint0=%7B%7D&waypoint1=%7B%7D",
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
            "description": "*Request a route preferring or avoiding specific types of road*\n\nRouting preferences can be added by extending the `mode` parameter of the request URL by adding a semi-colon delimited list of route link flags. In this case the addition of `motorway:-3` to the `mode` parameter indicates a strict exclusion of motorways. Consult the Routing API Reference for a full description of `mode` parameter and different feature weights.\n\n\n\n* **waypoint0**  `latlng`\n \\- Start point of the route.    e.g. `52.515,13.377`\n\n* **waypoint1**  `latlng`\n \\- Second point through which the route must pass.    e.g. `52.6172,13.3833`\n\n* **mode**  `text`\n \\- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83b27a4a-c135-4719-86a3-53fe26bfa047"
            }
          ]
        }
      ]
    }
  ]
}
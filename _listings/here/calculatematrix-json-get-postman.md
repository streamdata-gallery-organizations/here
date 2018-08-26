{
  "info": {
    "name": "HERE Routing API Many to many matrix routing",
    "_postman_id": "fef5eadf-77ec-4275-9d24-e329edce06ac",
    "description": "*Matrix routing request with three start points and five destinations*\n\nMatrix calculations are made using the `calculatematrix` endpoint and appending a three start parameters (`start0, ``start1, ``start2)` and multiple consecutively numbered `destination` parameters to the request.\n  \n\n\n\n* **start0**  `latlng`\n \\- First start point for the route calculations.    e.g. `52.515,13.377`  \n\n* **start1**  `latlng`\n \\- Second start point for the route calculations.    e.g. `52.515,13.377`  \n\n* **start2**  `latlng`\n \\- Third start point for the route calculations.    e.g. `52.515,13.377`  \n\n* **destination0**  `latlng`\n \\- First destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination1**  `latlng`\n \\- Second destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination2**  `latlng`\n \\- Third destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination3**  `latlng`\n \\- Fourth destination point for the route calculations.    e.g. `52.4,13.5`    \n\n* **destination4**  `latlng`\n \\- Fifth destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **mode**  `text`\n \\- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`  \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_id with every request.    \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Avoid",
      "item": [
        {
          "id": "be9998b5-8cc2-4605-a14f-0a4cd02eacbe",
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
              "id": "9cc136f6-6868-4caa-bf96-24ae6a3dd194"
            }
          ]
        }
      ]
    },
    {
      "name": "Many",
      "item": [
        {
          "id": "7c073ad4-824a-4b64-b558-6eb60a99a122",
          "name": "CalculatematrixJsonGet2",
          "request": {
            "url": "http://route.cit.api.here.com/routing/7.2/calculatematrix.json?app_code=%7B%7D&app_id=%7B%7D&destination0=%7B%7D&destination1=%7B%7D&destination2=%7B%7D&destination3=%7B%7D&destination4=%7B%7D&mode=%7B%7D&start0=%7B%7D&start1=%7B%7D&start2=%7B%7D",
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
            "description": "*Matrix routing request with three start points and five destinations*\n\nMatrix calculations are made using the `calculatematrix` endpoint and appending a three start parameters (`start0, ``start1, ``start2)` and multiple consecutively numbered `destination` parameters to the request.\n  \n\n\n\n* **start0**  `latlng`\n \\- First start point for the route calculations.    e.g. `52.515,13.377`  \n\n* **start1**  `latlng`\n \\- Second start point for the route calculations.    e.g. `52.515,13.377`  \n\n* **start2**  `latlng`\n \\- Third start point for the route calculations.    e.g. `52.515,13.377`  \n\n* **destination0**  `latlng`\n \\- First destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination1**  `latlng`\n \\- Second destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination2**  `latlng`\n \\- Third destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination3**  `latlng`\n \\- Fourth destination point for the route calculations.    e.g. `52.4,13.5`    \n\n* **destination4**  `latlng`\n \\- Fifth destination point for the route calculations.    e.g. `52.4,13.5`  \n\n* **mode**  `text`\n \\- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`  \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_id with every request.    \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0298e1c8-e9c8-4d55-b38d-6e53b0b345cc"
            }
          ]
        }
      ]
    }
  ]
}
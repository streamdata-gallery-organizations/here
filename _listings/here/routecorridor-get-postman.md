{
  "info": {
    "name": "HERE Custom Location Extension API Find Locations along a pre-defined Route",
    "_postman_id": "0ebae993-6210-4b15-87dd-dfde354e0f3b",
    "description": "*Request a list of user-defined locations along a pre-defined route*\n\nThe route has been pre-calculated and the `routeid` has already been acquired from a previous routing request. A route-based corridor search is requested using the `corridor` endpoint and by adding the `routeid` parameter to the request URL, along with a corridor `width`.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **routeId**  `text`\n \\- A <b>previously</b> calculated routeId\n\n* **radius**  `number`\n \\- Width of the search corridor\n\n* **limit**  `number`\n \\- The limit of the number of items contained in the response.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Find",
      "item": [
        {
          "id": "9c8e1cc7-0c28-43fe-8772-bf27534c6eaa",
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
              "id": "00642d22-0dcd-435c-85d3-74662e9deb4f"
            }
          ]
        },
        {
          "id": "9ba019cb-057b-4897-ab01-bce5a8b75d6b",
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
              "id": "7a33422c-29fc-49d8-9f6b-aac26a941f67"
            }
          ]
        },
        {
          "id": "af874d69-8306-4dbb-a322-99964035ab77",
          "name": "RouteCorridorGet",
          "request": {
            "url": "http://customlocation.cit.api.here.com/v1/search/route/corridor?app_code=%7B%7D&app_id=%7B%7D&layerId=%7B%7D&limit=%7B%7D&radius=%7B%7D&routeId=%7B%7D",
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
            "description": "*Request a list of user-defined locations along a pre-defined route*\n\nThe route has been pre-calculated and the `routeid` has already been acquired from a previous routing request. A route-based corridor search is requested using the `corridor` endpoint and by adding the `routeid` parameter to the request URL, along with a corridor `width`.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **routeId**  `text`\n \\- A <b>previously</b> calculated routeId\n\n* **radius**  `number`\n \\- Width of the search corridor\n\n* **limit**  `number`\n \\- The limit of the number of items contained in the response.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "971b80da-2e05-46d0-9409-bb68e5847594"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "HERE Places API Explore Nearby Places",
    "_postman_id": "a50c3477-7fc9-4c2c-a228-8de6843ddaaf",
    "description": "*Request a list of places close to a location *\n\nThe `discover/here` endpoint allow users to request a list of places near to a given point, based on a location precision parameter (in this case the `at` parameter) which must be provided. If the precision is high, the places around that point are returned in order of proximity. Otherwise a set of recommended places in the area is returned.\n\n\n\n* **at**  `latlng`\n \\- Location of the central point for the places search.    e.g. `52.515,13.377`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Accept**  `header`\n\n  Format to request from the server",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Search",
      "item": [
        {
          "id": "c1bc8ae6-f369-4dc1-b736-148e5f9496a2",
          "name": "SuggestGet",
          "request": {
            "url": "http://places.demo.api.here.com/places/v1/suggest?app_code=%7B%7D&app_id=%7B%7D&at=%7B%7D&q=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of suggestions based on a partial query string*\n\nA suggestions request can be made using the `suggest` endpoint in the request URL and adding the `q` parameter with the partial query string. The focal point for the suggestion service is defined using the `at` parameter.\n\n\n\n* **at**  `latlng`\n \\- Location of the central point for the places search.    e.g. `52.515,13.377`\n\n* **q**  `text`\n \\- Free-form text containing the search term.    e.g. `restaurant` or `Brandenburger Tor`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Accept**  `header`\n\n  Format to request from the server"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "beeb4182-8271-4756-bf01-363e56eb2676"
            }
          ]
        }
      ]
    },
    {
      "name": "Place",
      "item": [
        {
          "id": "c8f511e1-3808-49e7-8d29-b0a65b7fae23",
          "name": "CategoriesPlacesGet",
          "request": {
            "url": "http://places.demo.api.here.com/places/v1/categories/places?app_code=%7B%7D&app_id=%7B%7D&at=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of place categories available for a given location*\n\nA place category request can be made using the `categories/places` endpoint in the request URL and specifying the  focal point using the `at` parameter.\n\n\n\n* **at**  `latlng`\n \\- Location of the central point for the places search.    e.g. `52.515,13.377`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Accept**  `header`\n\n  Format to request from the server"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "28108b8d-db4b-4da5-b336-84a871593d71"
            }
          ]
        }
      ]
    },
    {
      "name": "Explore",
      "item": [
        {
          "id": "3800b024-3fae-4ab4-988e-117e33e7cbf2",
          "name": "DiscoverExploreGet5",
          "request": {
            "url": "http://places.demo.api.here.com/places/v1/discover/explore?app_code=%7B%7D&app_id=%7B%7D&at=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of popular places around a location*\n\nThe `explore` location context can either be an explicitly given location using the `at` parameter, or implicitly defined by a user's current position or the currently visible map.\n\n\n\n* **at**  `latlng`\n \\- Location of the central point for the places search.    e.g. `52.515,13.377`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Accept**  `header`\n\n  Format to request from the server"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f0f05cd8-4bd5-44a5-b843-1d094f17ee8e"
            }
          ]
        },
        {
          "id": "6a7eb784-9c69-4f95-bf6f-e228b73b97c2",
          "name": "DiscoverHereGet",
          "request": {
            "url": "http://places.demo.api.here.com/places/v1/discover/here?app_code=%7B%7D&app_id=%7B%7D&at=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of places close to a location *\n\nThe `discover/here` endpoint allow users to request a list of places near to a given point, based on a location precision parameter (in this case the `at` parameter) which must be provided. If the precision is high, the places around that point are returned in order of proximity. Otherwise a set of recommended places in the area is returned.\n\n\n\n* **at**  `latlng`\n \\- Location of the central point for the places search.    e.g. `52.515,13.377`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Accept**  `header`\n\n  Format to request from the server"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "309f62cc-e4e6-4a4e-8528-7c21754f0fbf"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "HERE Places API Search Suggestions",
    "_postman_id": "89cb7818-fe40-473c-9835-2768dae3262e",
    "description": "*Request a list of suggestions based on a partial query string*\n\nA suggestions request can be made using the `suggest` endpoint in the request URL and adding the `q` parameter with the partial query string. The focal point for the suggestion service is defined using the `at` parameter.\n\n\n\n* **at**  `latlng`\n \\- Location of the central point for the places search.    e.g. `52.515,13.377`\n\n* **q**  `text`\n \\- Free-form text containing the search term.    e.g. `restaurant` or `Brandenburger Tor`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Accept**  `header`\n\n  Format to request from the server",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Search",
      "item": [
        {
          "id": "d5c34082-95e8-49e1-8c26-876b46454ee9",
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
              "id": "409928e5-9fc3-4339-b6b7-7908bdf9c1bd"
            }
          ]
        }
      ]
    }
  ]
}
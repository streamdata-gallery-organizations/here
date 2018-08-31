{
  "info": {
    "name": "HERE Places API Place Categories",
    "_postman_id": "a5948c9a-21e2-4a14-b890-b98eaa003fea",
    "description": "*Request a list of place categories available for a given location*\n\nA place category request can be made using the `categories/places` endpoint in the request URL and specifying the  focal point using the `at` parameter.\n\n\n\n* **at**  `latlng`\n \\- Location of the central point for the places search.    e.g. `52.515,13.377`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Accept**  `header`\n\n  Format to request from the server",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Place",
      "item": [
        {
          "id": "efd42c55-3020-4286-8a09-499f44fff829",
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
              "id": "fc523355-d6c5-4a84-8605-71351aa3e20e"
            }
          ]
        }
      ]
    }
  ]
}
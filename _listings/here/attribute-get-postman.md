{
  "info": {
    "name": "HERE Custom Location Extension API Filtering by Custom Attributes",
    "_postman_id": "9dc01f98-4dcd-4dc2-943d-2ef1402b16ab",
    "description": "*Request a list of user-defined locations based on their attribute values*\n\nAn attribute-based search is requested using the `attribute` endpoint and by adding the `query` parameter to the request URL.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **query**  `text`\n \\- The query to retrieve\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Filtering",
      "item": [
        {
          "id": "1e0f0289-8d5d-48da-9cc1-df357b55e427",
          "name": "AttributeGet",
          "request": {
            "url": "http://customlocation.cit.api.here.com/v1/search/attribute?app_code=%7B%7D&app_id=%7B%7D&layerId=%7B%7D&query=%7B%7D",
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
            "description": "*Request a list of user-defined locations based on their attribute values*\n\nAn attribute-based search is requested using the `attribute` endpoint and by adding the `query` parameter to the request URL.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **query**  `text`\n \\- The query to retrieve\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b85f3466-51f3-4007-a0c2-6ebd49572fd3"
            }
          ]
        }
      ]
    }
  ]
}
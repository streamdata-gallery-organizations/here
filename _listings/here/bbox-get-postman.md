{
  "info": {
    "name": "HERE Custom Location Extension API Find Locations within a Bounding Box",
    "_postman_id": "943922c8-0355-42a4-b23d-b1e0b293cbf6",
    "description": "*Request a list of user-defined locations within a defined area*\n\nThe request uses the `bbox` endpoint, and the bounding box is specified by adding the `bbox` parameter to the request URL.\n\n\n\n* **layerId**  `text`\n \\- Unique indicator used to retrieve a dataset\n\n* **bbox**  `bbox`\n \\- Restricts results to be found within this bounding box\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Find",
      "item": [
        {
          "id": "68ecfdc4-bc70-4761-965d-06cb68a10b90",
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
              "id": "0bfc0344-3066-4890-9be8-0de8d548d7c8"
            }
          ]
        }
      ]
    }
  ]
}
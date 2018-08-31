{
  "info": {
    "name": "HERE Batch Geocoder API Get Job",
    "_postman_id": "5c7af6fb-c437-4bee-a2d5-6b96a293a9c6",
    "description": "*Request the status of a batch geocoder job*\n\nTo check the status, make a request to the `jobs` endpoint  appending the `requestId` and using the parameter `action=status `\n  \n\n\n\n* **action**  `enum`\n \\- Type of request  \n\n Valid values are : `cancel`, `runs`, `status`\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.  \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Job",
      "item": [
        {
          "id": "4528b93e-f14b-4bdf-af07-2679f64a1e73",
          "name": "getJob",
          "request": {
            "url": "http://batch.geocoder.cit.api.here.com/6.2/jobs/puwWrv32YOU24y8MNoUr793chFAI36aC?action=%7B%7D&app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request the status of a batch geocoder job*\n\nTo check the status, make a request to the `jobs` endpoint  appending the `requestId` and using the parameter `action=status `\n  \n\n\n\n* **action**  `enum`\n \\- Type of request  \n\n Valid values are : `cancel`, `runs`, `status`\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.  \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a4f35eb9-700d-40aa-87fb-bd8a3584b380"
            }
          ]
        }
      ]
    }
  ]
}
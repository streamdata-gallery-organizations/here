{
  "info": {
    "name": "HERE Traffic API Traffic Flow Availability Data",
    "_postman_id": "a780bd08-f90a-4874-9eb8-cd7ee650038d",
    "description": "*Flow availability requests allow you to see what traffic flow coverage exists in the current Traffic API.*\n\nT<i></i>he Server also supports an XML response.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Traffic",
      "item": [
        {
          "id": "a16e8c9a-f098-4908-aa53-388774c2ff71",
          "name": "60FlowavailabilityJsonGet",
          "request": {
            "url": "http://tiles.traffic.cit.api.here.com/traffic/6.0/tiles/8/133/86/256/6.0/flowavailability.json?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Flow availability requests allow you to see what traffic flow coverage exists in the current Traffic API.*\n\nT<i></i>he Server also supports an XML response.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0657dc3e-794d-4933-bec6-eaa819b45058"
            }
          ]
        }
      ]
    }
  ]
}
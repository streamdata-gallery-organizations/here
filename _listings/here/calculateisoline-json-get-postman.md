{
  "info": {
    "name": "HERE Routing API Time-based isoline with destination as center",
    "_postman_id": "5a5f7e5d-e8aa-4ce7-b15e-7d448b416bcb",
    "description": "*Request an isoline that will reach a destination within a given time*\n\nTime-based reverse flow requests are made using the `calculateisoline` endpoint and specifying the `destination` and `rangetype=time` parameters.\n\n\n\n* **mode**  `text`\n \\- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`\n\n* **destination**  `latlng`\n \\- Destination of the reverse flow calculation.    e.g. `52.515,13.377`\n\n* **rangetype**  `text`\n \\- Specifies type of range. Possible values are distance, time. For distance the unit is  meters. For time the unit is seconds.  rangetype=distance  rangetype=time    \n\n* **range**  `number`\n \\- Range of isoline. Several comma separated values can be specified. The unit is defined by  parameter rangetype  range=1000  range=1000,2000,3000  \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.  \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Time-based",
      "item": [
        {
          "id": "255e131e-1904-4dc3-9c3c-9c52a109e48b",
          "name": "CalculateisolineJsonGet4",
          "request": {
            "url": "http://route.cit.api.here.com/routing/7.2/calculateisoline.json?app_code=%7B%7D&app_id=%7B%7D&destination=%7B%7D&mode=%7B%7D&range=%7B%7D&rangetype=%7B%7D",
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
            "description": "*Request an isoline that will reach a destination within a given time*\n\nTime-based reverse flow requests are made using the `calculateisoline` endpoint and specifying the `destination` and `rangetype=time` parameters.\n\n\n\n* **mode**  `text`\n \\- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`\n\n* **destination**  `latlng`\n \\- Destination of the reverse flow calculation.    e.g. `52.515,13.377`\n\n* **rangetype**  `text`\n \\- Specifies type of range. Possible values are distance, time. For distance the unit is  meters. For time the unit is seconds.  rangetype=distance  rangetype=time    \n\n* **range**  `number`\n \\- Range of isoline. Several comma separated values can be specified. The unit is defined by  parameter rangetype  range=1000  range=1000,2000,3000  \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.  \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "abf44a6c-489d-440d-9cf5-510ecb54fa59"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "HERE Public Transit API Reachability of an Area Within a Specific Time",
    "_postman_id": "5725c99f-463e-4f90-917e-3918a4e776c1",
    "description": "*Request a list of the public transit stations that can be reached in a given time*\n\nTo find the stations reachable in a specified time use the `isochrone/v1/search.json` endpoint specifying a center point using the `x` and `y` parameters and a maximum total duration in minutes using the `max_dur `parameter.\n  \n\n\n\n* **max_dur**  `number`\n \\- Maximum duration of the journeys, in minutes.   Minimum = 5, Maximum = 90.    The default duration is 15 minutes.    \n\n* **y**  `number`\n \\- The latitude of the start point of your journey.    e.g. `52.515`  \n\n* **x**  `number`\n \\- The longitude of the start point of your journey.    e.g. `13.377`    \n\n* **time**  `text`\n \\- Specifies the time in ISO 8601 (for example, 2015-10-18T06:36:40)\n        format. \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Reachability",
      "item": [
        {
          "id": "14c02fa1-2cd7-475e-9fb9-0f22b7af4908",
          "name": "IsochroneV1SearchJsonGet2",
          "request": {
            "url": "http://cit.transit.api.here.com/isochrone/v1/search.json?app_code=%7B%7D&app_id=%7B%7D&max_dur=%7B%7D&time=%7B%7D&x=%7B%7D&y=%7B%7D",
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
            "description": "*Request a list of the public transit stations that can be reached in a given time*\n\nTo find the stations reachable in a specified time use the `isochrone/v1/search.json` endpoint specifying a center point using the `x` and `y` parameters and a maximum total duration in minutes using the `max_dur `parameter.\n  \n\n\n\n* **max_dur**  `number`\n \\- Maximum duration of the journeys, in minutes.   Minimum = 5, Maximum = 90.    The default duration is 15 minutes.    \n\n* **y**  `number`\n \\- The latitude of the start point of your journey.    e.g. `52.515`  \n\n* **x**  `number`\n \\- The longitude of the start point of your journey.    e.g. `13.377`    \n\n* **time**  `text`\n \\- Specifies the time in ISO 8601 (for example, 2015-10-18T06:36:40)\n        format. \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "188f1e0b-cedc-4dd0-82f4-1290ebb5ca4f"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "HERE Public Transit API All Next Departures (deprecated)",
    "_postman_id": "ec0567db-5443-45fd-a4ce-8f1df28285d2",
    "description": "*Request a list of all next departure times and destinations from a location.*\n\nAll next departures information can be requested using the `metarouter/rest/boardservice/v1/multiboard.json` and specifying a `time` and `coordinates. `The maximum numbers of nearby stations and number of departures per station can be restricted by using the `max_stn` and `max` parameters, respectively.\n  \n  <b>NOTE:</b> This API has been deprecated and replaced with 2 new endpoints. Please see \n  <b><i>All Next Departures from a Location </i></b>and <b><i>All Next Departures for a list of Stations </i></b>for more details.\n  \n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **startX**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number of next departures per station to be included in the response.    The default value is 40.  \n\n* **max_stn**  `text`\n \\-  The maximum number of stations for which departures are required. The default value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit binary number, where each bit represents one type of transit.  \n  0: High-speed Trains  \n  1: Intercity/EuroCity Trains  \n  2: Inter-regional and fast trains  \n  3: Regional and other trains  \n  4: City trains  \n  5: Buses  \n  6: Boat/Ferries  \n  7: Metro/Subway  \n  8: Tram  \n  9: Ordered services/Taxi  \n  10: Inclined/Funicular  \n  11: Aerial/Cable Car  \n  12: Rapid Bus  \n  13: Monorail  \n  14: Air plane  \n  15: Not yet defined  \n  The default is 1111111111111111, meaning all supported transit types are permitted.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "All",
      "item": [
        {
          "id": "2855435e-fa87-4573-9c4d-7e3271345614",
          "name": "MetarouterRestBoardserviceV1MultiboardJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/metarouter/rest/boardservice/v1/multiboard.json?app_code=%7B%7D&app_id=%7B%7D&lang=%7B%7D&max=%7B%7D&max_stn=%7B%7D&prod=%7B%7D&startX=%7B%7D&startY=%7B%7D&time=%7B%7D",
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
            "description": "*Request a list of all next departure times and destinations from a location.*\n\nAll next departures information can be requested using the `metarouter/rest/boardservice/v1/multiboard.json` and specifying a `time` and `coordinates. `The maximum numbers of nearby stations and number of departures per station can be restricted by using the `max_stn` and `max` parameters, respectively.\n  \n  <b>NOTE:</b> This API has been deprecated and replaced with 2 new endpoints. Please see \n  <b><i>All Next Departures from a Location </i></b>and <b><i>All Next Departures for a list of Stations </i></b>for more details.\n  \n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **startX**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number of next departures per station to be included in the response.    The default value is 40.  \n\n* **max_stn**  `text`\n \\-  The maximum number of stations for which departures are required. The default value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit binary number, where each bit represents one type of transit.  \n  0: High-speed Trains  \n  1: Intercity/EuroCity Trains  \n  2: Inter-regional and fast trains  \n  3: Regional and other trains  \n  4: City trains  \n  5: Buses  \n  6: Boat/Ferries  \n  7: Metro/Subway  \n  8: Tram  \n  9: Ordered services/Taxi  \n  10: Inclined/Funicular  \n  11: Aerial/Cable Car  \n  12: Rapid Bus  \n  13: Monorail  \n  14: Air plane  \n  15: Not yet defined  \n  The default is 1111111111111111, meaning all supported transit types are permitted."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0db70e51-1a02-442d-8465-d5fe6f1c7c57"
            }
          ]
        }
      ]
    }
  ]
}
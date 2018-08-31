{
  "info": {
    "name": "HERE Map Tile API Filtering Points of Interest",
    "_postman_id": "24da2458-534c-4ad5-a264-228b7a2aea3a",
    "description": "*Request a map tile including selected points of interest*\n\nPoints of interest are displayed by passing the `pois` parameter in the request URL. The type of points of interest to be displayed can be filtered by using a hexadecimal bitmask.\n  \n\n\n\n* **pois**  `text`\n \\- Displays points of interest if present  \n\n Valid values are : `default`, `alps`, `fleet`, `wings`, `dreamworks`, `flame`, `mini`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Filtering",
      "item": [
        {
          "id": "ca84cb4c-c9f7-467b-a6f7-c90ee8f15b9a",
          "name": "MaptileNewestNormalDay161874325072256Png8Get3",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/16/18743/25072/256/png8?app_code=%7B%7D&app_id=%7B%7D&pois=%7B%7D",
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
            "description": "*Request a map tile including selected points of interest*\n\nPoints of interest are displayed by passing the `pois` parameter in the request URL. The type of points of interest to be displayed can be filtered by using a hexadecimal bitmask.\n  \n\n\n\n* **pois**  `text`\n \\- Displays points of interest if present  \n\n Valid values are : `default`, `alps`, `fleet`, `wings`, `dreamworks`, `flame`, `mini`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60deddb9-55ed-49f2-b3c2-99c7e0d645d9"
            }
          ]
        }
      ]
    }
  ]
}
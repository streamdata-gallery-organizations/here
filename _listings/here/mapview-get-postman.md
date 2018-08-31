{
  "info": {
    "name": "HERE Map Image API Map Image using Bounding Box",
    "_postman_id": "bb964bda-462d-4536-8703-27020c8b1ef8",
    "description": "*Request an image of a map based around a given area*\n\nTo specify a bounding box, add the `bbox` parameter to the request URL. On desktop browsers, redirection to `here.com` will occur automatically unless the `nord` parameter is also added to URL.\n\n\n\n* **bbox**  `text`\n \\- Bounding box of the map specifying the top-right and bottom left corners.    e.g. `52.515,13.377,52.134,13.978`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Map",
      "item": [
        {
          "id": "234d6d80-c9cd-4250-a5e8-bc527965ef9e",
          "name": "MapviewGet15",
          "request": {
            "url": "http://image.maps.cit.api.here.com/mia/1.6/mapview?app_code=%7B%7D&app_id=%7B%7D&bbox=%7B%7D",
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
            "description": "*Request an image of a map based around a given area*\n\nTo specify a bounding box, add the `bbox` parameter to the request URL. On desktop browsers, redirection to `here.com` will occur automatically unless the `nord` parameter is also added to URL.\n\n\n\n* **bbox**  `text`\n \\- Bounding box of the map specifying the top-right and bottom left corners.    e.g. `52.515,13.377,52.134,13.978`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "721a79cb-3ae3-42b5-a553-807911449920"
            }
          ]
        },
        {
          "id": "6bd879c3-e3bb-4b64-a4fb-33d552c7310b",
          "name": "RouteGet",
          "request": {
            "url": "http://image.maps.cit.api.here.com/mia/1.6/route?app_code=%7B%7D&app_id=%7B%7D&lc0=%7B%7D&lc1=%7B%7D&lw0=%7B%7D&lw1=%7B%7D&m0=%7B%7D&m1=%7B%7D&r0=%7B%7D&r1=%7B%7D&sc0=%7B%7D&sc1=%7B%7D&w=%7B%7D",
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
            "description": "*Request an image of a map including a polyline*\n\nIt supports also different map schemes, image sizes; image formats as \r\nwell as zooming out from automatically calculated zoom level.\n  \n\n\n\n* **r0**  `text`\n \\- List of coordinates describing the first route\n\n* **r1**  `text`\n \\- List of coordinates describing the second route\n\n* **m0**  `text`\n \\- First route marker on the map\n\n* **m1**  `text`\n \\- Second route marker on the map\n\n* **lc0**  `text`\n \\- Color of the first route line displayed on the map\n\n* **sc0**  `text`\n \\- Shadow color of the first route line displayed on the map\n\n* **lw0**  `number`\n \\- Width of the first route line displayed on the map\n\n* **lc1**  `text`\n \\- Color of the second route line displayed on the map\n\n* **sc1**  `text`\n \\- Shadow color of the second route line displayed on the map\n\n* **lw1**  `number`\n \\- Width of the second route line displayed on the map\n\n* **w**  `number`\n \\- Image width in pixels, maximum 2048.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f173c323-2d8e-45f4-b091-443bcce6bb09"
            }
          ]
        }
      ]
    }
  ]
}
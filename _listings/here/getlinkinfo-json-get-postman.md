{
  "info": {
    "name": "HERE Routing API Link Information using linkId",
    "_postman_id": "4cde6b11-c1cb-4c2a-b049-0f0e13b7018e",
    "description": "*Request detailed information about a path segment in the routing network given a linkid*\n\nLink information can be retrieved using the `getlinkinfo` endpoint, by specifying one or more comma separated linkIds using the `linkids` parameter. The `linkids` have been generated from a previous request. Note that positive direction '+' in link Ids has to be URL encoded.\n  \n  \n\n\n\n* **linkids**  `text`\n \\- Link identifiers for which the detailed information is being requested.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Link",
      "item": [
        {
          "id": "ea9777fa-a321-4dda-b17a-9629725540a2",
          "name": "GetlinkinfoJsonGet2",
          "request": {
            "url": "http://route.cit.api.here.com/routing/7.2/getlinkinfo.json?app_code=%7B%7D&app_id=%7B%7D&linkids=%7B%7D",
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
            "description": "*Request detailed information about a path segment in the routing network given a linkid*\n\nLink information can be retrieved using the `getlinkinfo` endpoint, by specifying one or more comma separated linkIds using the `linkids` parameter. The `linkids` have been generated from a previous request. Note that positive direction '+' in link Ids has to be URL encoded.\n  \n  \n\n\n\n* **linkids**  `text`\n \\- Link identifiers for which the detailed information is being requested.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aae1109e-905a-4557-a808-c46d4babe818"
            }
          ]
        }
      ]
    }
  ]
}
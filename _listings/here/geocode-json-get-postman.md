{
  "info": {
    "name": "HERE Geocoder API Geocode using partial address information",
    "_postman_id": "6a83e258-43a6-497a-bdfd-a954a26edf04",
    "description": "*Request the latitude, longitude and details of an address based on partial address information*\n\nThis example shows a structured (qualified) geocoding request using the `geocode` endpoint. In this structured request the data is provided in `country`, `city`, `street` and `housenumber` parameters in the request URL. Note that the street name misses the directional (\"W\") and also the street type. The omitted directional makes the query ambiguous and the response contains therefore two results: One address on West Randolph St and one on East Randolph St.\n  \n\n\n\n* **housenumber**  `text`\n \\- The house number or house name\n\n* **street**  `text`\n \\- The street name can include suite, apt and floor information.\n\n* **city**  `text`\n \\- City name\n\n* **country**  `text`\n \\- Specify the country or list of countries using the country code (3 bytes, ISO 3166-1-alpha-3) or the country name\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Geocode",
      "item": [
        {
          "id": "9ed53340-48c9-42a2-bd1a-40cf6345739c",
          "name": "GeocodeJsonGet5",
          "request": {
            "url": "http://geocoder.cit.api.here.com/6.2/geocode.json?app_code=%7B%7D&app_id=%7B%7D&city=%7B%7D&country=%7B%7D&gen=%7B%7D&housenumber=%7B%7D&street=%7B%7D",
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
            "description": "*Request the latitude, longitude and details of an address based on partial address information*\n\nThis example shows a structured (qualified) geocoding request using the `geocode` endpoint. In this structured request the data is provided in `country`, `city`, `street` and `housenumber` parameters in the request URL. Note that the street name misses the directional (\"W\") and also the street type. The omitted directional makes the query ambiguous and the response contains therefore two results: One address on West Randolph St and one on East Randolph St.\n  \n\n\n\n* **housenumber**  `text`\n \\- The house number or house name\n\n* **street**  `text`\n \\- The street name can include suite, apt and floor information.\n\n* **city**  `text`\n \\- City name\n\n* **country**  `text`\n \\- Specify the country or list of countries using the country code (3 bytes, ISO 3166-1-alpha-3) or the country name\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "307a726b-0158-4181-88f0-9e5914321078"
            }
          ]
        }
      ]
    }
  ]
}
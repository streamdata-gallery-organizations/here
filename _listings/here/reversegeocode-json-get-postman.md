{
  "info": {
    "name": "HERE Geocoder API Reverse Geocode Landmarks",
    "_postman_id": "a19e6542-aad3-4cd7-9a20-ca03f769847a",
    "description": "*Request details of landmarks near to a given latitude and longitude*\n\nLandmark reverse geocoding requests can be made using the `reversegeocode` endpoint, specifying the parameter `mode=retrieveLandmarks`, and adding the `prox` parameter to the request URL.  Consult the  Geocoder API Reference for a full list of available landmark types.\n\n\n\n* **prox**  `prox`\n \\- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`\n\n* **mode**  `enum`\n \\- Type of search invoked. Search for streets, administrative areas or landmarks, or a combination of all three\n\n Valid values are : `retrieveAddresses`, `retrieveAreas`, `retrieveLandmarks`, `retrieveAll`, `trackPosition`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible behavior in the API",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Geocode",
      "item": [
        {
          "id": "0fa121c0-c41d-4111-b804-6c1a41c8de81",
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
              "id": "bcbb59cd-2df7-48c1-8f41-8ca57c005800"
            }
          ]
        }
      ]
    },
    {
      "name": "Reverse",
      "item": [
        {
          "id": "745bd35b-d4ab-461b-a337-ea233707eb99",
          "name": "ReversegeocodeJsonGet4",
          "request": {
            "url": "http://geocoder.cit.api.here.com/6.2/reversegeocode.json?app_code=%7B%7D&app_id=%7B%7D&gen=%7B%7D&mode=%7B%7D&prox=%7B%7D",
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
            "description": "*Request details of landmarks near to a given latitude and longitude*\n\nLandmark reverse geocoding requests can be made using the `reversegeocode` endpoint, specifying the parameter `mode=retrieveLandmarks`, and adding the `prox` parameter to the request URL.  Consult the  Geocoder API Reference for a full list of available landmark types.\n\n\n\n* **prox**  `prox`\n \\- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`\n\n* **mode**  `enum`\n \\- Type of search invoked. Search for streets, administrative areas or landmarks, or a combination of all three\n\n Valid values are : `retrieveAddresses`, `retrieveAreas`, `retrieveLandmarks`, `retrieveAll`, `trackPosition`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible behavior in the API"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30666cda-bc95-4f8e-be66-54d5769c1779"
            }
          ]
        }
      ]
    }
  ]
}
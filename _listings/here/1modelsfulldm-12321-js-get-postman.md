{
  "info": {
    "name": "HERE Venue Maps Full Venue Model",
    "_postman_id": "214abe09-093b-4b2d-b55f-f47fd59c9ca2",
    "description": "*Request extended details of places found within a venue*\n\nA full model of a venue can be obtained by passing `models-full` in the path of the request URL and appending the `id` of the venue in question along with associated authentication credentials. \n  \n  Note that the client-side process formatting the JSON response may take some time in older browsers.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n \\- Key-Pair-Id",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Base64",
      "item": [
        {
          "id": "31a155c8-8a47-4805-b6cb-5438ff3be685",
          "name": "0TilesIaB64L112022001101210030210JsGet",
          "request": {
            "url": "http://signature.venue.maps.cit.api.here.com/venues/signature/0/tiles-ia-b64/L1/12022001101210030210.js?app_code=%7B%7D&app_id=%7B%7D&Key-Pair-Id=%7B%7D&Policy=%7B%7D&Signature=%7B%7D",
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
            "description": "*Request a base64 encoded map tile and associated room definitions with a single request*\n\nA base64 encoded map tile together with the room definitions, is requested by passing `tiles-ia-b64` in the path of the request URL, along with a known `floor` and `quadkey` and associated authentication credentials.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n \\- Key-Pair-Id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5a794c8a-1417-4fae-9b90-172d7597dd0f"
            }
          ]
        }
      ]
    },
    {
      "name": "Room",
      "item": [
        {
          "id": "8ee27de2-172e-4f8f-b6a6-bde7a4efac29",
          "name": "0TilesIaL112022001101210030210JsGet",
          "request": {
            "url": "http://signature.venue.maps.cit.api.here.com/venues/signature/0/tiles-ia/L1/12022001101210030210.js?app_code=%7B%7D&app_id=%7B%7D&Key-Pair-Id=%7B%7D&Policy=%7B%7D&Signature=%7B%7D",
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
            "description": "*Request a list of the name and shape of rooms found within a single venue map tile*\n\nRoom data associated with a map tile is requested by passing `tiles-ia` in the path of the request URL, along with a known `floor` and `quadkey` and associated authentication credentials.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n \\- Key-Pair-Id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d062bff1-0fa9-4b5c-800f-fdbc9d3ae525"
            }
          ]
        }
      ]
    },
    {
      "name": "Venue",
      "item": [
        {
          "id": "aeb9cbff-a03e-44cd-8e47-7ac2217df1b7",
          "name": "0TilesPngL112022001101210030210PngGet",
          "request": {
            "url": "http://signature.venue.maps.cit.api.here.com/venues/signature/0/tiles-png/L1/12022001101210030210.png?app_code=%7B%7D&app_id=%7B%7D&Key-Pair-Id=%7B%7D&Policy=%7B%7D&Signature=%7B%7D",
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
            "description": "*Request an individual venue map tile*\n\nIn addition to the usual `app_id` and `app_code`, three additional parameters are required for authentication purposes. The `Signature`, `Policy` and `Key-Pair-Id` parameters have been obtained from a prior request to the `Signature` endpoint.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n \\- Key-Pair-Id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70f5623c-10dc-430f-890c-1c54ad2535a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Full",
      "item": [
        {
          "id": "b96e9d8c-df41-4ecc-8168-7871359d5f7b",
          "name": "1ModelsFullDM12321JsGet",
          "request": {
            "url": "http://signature.venue.maps.cit.api.here.com/venues/signature/1/models-full/DM_12321.js?app_code=%7B%7D&app_id=%7B%7D&Key-Pair-Id=%7B%7D&Policy=%7B%7D&Signature=%7B%7D",
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
            "description": "*Request extended details of places found within a venue*\n\nA full model of a venue can be obtained by passing `models-full` in the path of the request URL and appending the `id` of the venue in question along with associated authentication credentials. \n  \n  Note that the client-side process formatting the JSON response may take some time in older browsers.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n \\- Key-Pair-Id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c33a314f-0b8c-4e59-b9cb-de3a3f7292ae"
            }
          ]
        }
      ]
    }
  ]
}
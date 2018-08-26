{
  "info": {
    "name": "HERE Venue Maps Places within a Venue",
    "_postman_id": "1ea6e45c-82bf-4493-bc45-650706dd7b1b",
    "description": "*Request a list of the places within a venue*\n\nDetails of the individual places to be found within a venue can be obtained by passing `models-poi` in the path of the request URL and appending the `id` of the venue in question along with associated authentication credentials.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n \\- Key-Pair-Id",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Base64",
      "item": [
        {
          "id": "966c6575-cbea-42fe-a0ab-95cda0953b95",
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
              "id": "709b596b-d76a-4c6e-a70c-974de20ebec6"
            }
          ]
        }
      ]
    },
    {
      "name": "Room",
      "item": [
        {
          "id": "36dd34d5-51df-4bd5-a248-dfc161fcff7b",
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
              "id": "63981852-39df-4c86-ba4d-ba8d16235bf5"
            }
          ]
        }
      ]
    },
    {
      "name": "Venue",
      "item": [
        {
          "id": "b0b80f14-81a8-4055-83a8-bf8c3dd0495a",
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
              "id": "81d315be-7a4b-40cc-b8ac-6e21534099df"
            }
          ]
        }
      ]
    },
    {
      "name": "Full",
      "item": [
        {
          "id": "950162ab-9382-489f-9ae2-1a85009c716a",
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
              "id": "b2949050-3dfb-4095-aedd-fab0430f49e4"
            }
          ]
        }
      ]
    },
    {
      "name": "Places",
      "item": [
        {
          "id": "c83224cb-dc34-4179-b6db-205d62a1ce4c",
          "name": "1ModelsPoiDM7205JsGet",
          "request": {
            "url": "http://signature.venue.maps.cit.api.here.com/venues/signature/1/models-poi/DM_7205.js?app_code=%7B%7D&app_id=%7B%7D&Key-Pair-Id=%7B%7D&Policy=%7B%7D&Signature=%7B%7D",
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
            "description": "*Request a list of the places within a venue*\n\nDetails of the individual places to be found within a venue can be obtained by passing `models-poi` in the path of the request URL and appending the `id` of the venue in question along with associated authentication credentials.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.\n\n* **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n \\- Key-Pair-Id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "749570a0-4cb5-4339-acf1-cc08d561baf9"
            }
          ]
        }
      ]
    }
  ]
}
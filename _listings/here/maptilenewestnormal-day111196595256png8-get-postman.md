{
  "info": {
    "name": "HERE Map Tile API Foreign Language Support",
    "_postman_id": "5a779a74-c2a5-4322-8c29-071a15ba1728",
    "description": "*Request a map tile with labels in a foreign language*\n\nThe `lg` query parameter is used to define the language used on the map tiles. Consult the  Map Tile API Reference for a full list of available languages.\n\n\n\n* **lg**  `enum`\n \\- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Terrain",
      "item": [
        {
          "id": "1597986a-f009-41c6-8fc4-e2ddcfd0c494",
          "name": "TerrainDay76645256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/terrain.day/7/66/45/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a terrain map tile*\n\nTerrain map tile are available by passing `terrain.day` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6e1ebbf3-7b40-4953-ad06-1875715eba6c"
            }
          ]
        }
      ]
    },
    {
      "name": "Multiple",
      "item": [
        {
          "id": "8ab1db22-91de-41bf-9890-6f9d64804830",
          "name": "MaptileNewestNormalDay63024256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/6/30/24/256/png8?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D&range=%7B%7D",
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
            "description": "*Request multiple base64 encoded map tiles*\n\nA square consisting of multiple base64 encoded tiles is requested by adding the parameters `output=base64` and `range=NxN` to the request URL. The `column` and `row` in the path of the URL, defining the top left-hand corner of the tile group must be divisible by the value of the `range` parameter.\n  \n  Click on the response to decode the tiles returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return the tile as base64 encoded text.\n\n* **range**  `enum`\n \\- Indicates the size of the array of tiles returned. Valid values are `2x2`, `3x3` or `4x4`\n\n Valid values are : `2x2`, `3x3`, `4x4`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b5aeaae-c1a2-44a6-8158-34c557f2b003"
            }
          ]
        }
      ]
    },
    {
      "name": "Color-reduced",
      "item": [
        {
          "id": "18c2e952-25ef-44d3-8ca3-504a1177df3c",
          "name": "MaptileNewestNormalDayTransit1220741409256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day.transit/12/2074/1409/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a color-reduced map tile with public transport*\n\nColor-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0074b505-dbec-4279-89f0-0940c74e9bbc"
            }
          ]
        }
      ]
    },
    {
      "name": "Filtering",
      "item": [
        {
          "id": "f7dbea94-8406-46bd-be47-f38af7755f2e",
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
              "id": "e7871ed7-7b94-4196-a575-1f42358ff669"
            }
          ]
        }
      ]
    },
    {
      "name": "Hybrid",
      "item": [
        {
          "id": "135bfa29-b450-49f2-a5aa-19c34721b4c4",
          "name": "HybridDay485256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/hybrid.day/4/8/5/256/png8?app_code=%7B%7D&app_id=%7B%7D&lg=%7B%7D",
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
            "description": "*Request a hybrid map tile - satellite imagery with labels*\n\nHybrid map tile are available by passing `hybrid.day` in the path of the request URL. The map tiles will display using the default language of the server unless the `lg` query parameter is used to change the map tile language. Consult the  Map Tile API Reference for a full list of available languages.\n\n\n\n* **lg**  `enum`\n \\- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8f5cd9cf-fa59-4630-8ced-f59ed7ad25e5"
            }
          ]
        }
      ]
    },
    {
      "name": "Truck",
      "item": [
        {
          "id": "cc95a435-dd81-4be5-b6ed-dbea942108b6",
          "name": "TrucktileNewestNormalDay1221991342256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/trucktile/newest/normal.day/12/2199/1342/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a street map tile showing restrictions for heavy vehicles*\n\nTo obtain a map tile displaying route restrictions for trucks, use the `trucktile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ff1380b-1737-4e4c-81cc-e2ecf47a3622"
            }
          ]
        }
      ]
    },
    {
      "name": "Toll",
      "item": [
        {
          "id": "c5d98771-fcfd-4459-a259-4cb56261e22c",
          "name": "MaptileNewestNormalDay9255170256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/9/255/170/256/png8?app_code=%7B%7D&app_id=%7B%7D&congestion=%7B%7D",
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
            "description": "*Request a street map tile highlighting congestion and environmental toll zones*\n\nTo highlight such toll zones, add the `congestion` parameter to the request URL.\n\n\n\n* **congestion**  `null`\n \\- Flag to indicate if congestion zones are to be shown on the map.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4402d36-9553-4951-99bf-91eaa42f6454"
            }
          ]
        }
      ]
    },
    {
      "name": "Point",
      "item": [
        {
          "id": "866237a0-b86e-475f-84ba-b261807da253",
          "name": "MetaPoisGet",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/meta/pois?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D",
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
            "description": "*Request point of interest category information*\n\nTo make a request for point-of-interest information, use `meta/pois` in the path of the request URL.\n  \n\n\n\n* **output**  `enum`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n Valid values are : `json`, `text`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request..  \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a542d27c-249f-4e60-8890-e88ab2a0e6bc"
            }
          ]
        }
      ]
    },
    {
      "name": "Copyright",
      "item": [
        {
          "id": "1f886d75-254c-47de-9e5a-026f88763a90",
          "name": "CopyrightNewestGet",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/copyright/newest?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request map tile copyright information*\n\nTo make a request for copyright information, use the `copyright` parameter in the path of the request URL.\n  \n  Note that the client-side process formatting the JSON response may take some time in older browsers.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c010f249-6618-4e78-9171-a93d44ebad3d"
            }
          ]
        }
      ]
    },
    {
      "name": "Satellite",
      "item": [
        {
          "id": "e8dde6ee-f83c-4c93-ab75-61b8c53e95b8",
          "name": "SatelliteDay51512256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/satellite.day/5/15/12/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a satellite map tile*\n\nSatellite map tiles do not display labels and are available by passing `satellite.day` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97d6498a-0c8c-4145-bc75-d35edbaacd26"
            }
          ]
        }
      ]
    },
    {
      "name": "Foreign",
      "item": [
        {
          "id": "0e055d01-59e7-4bca-b7b4-a10ae610ec69",
          "name": "MaptileNewestNormalDay111196595256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/11/1196/595/256/png8?app_code=%7B%7D&app_id=%7B%7D&lg=%7B%7D",
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
            "description": "*Request a map tile with labels in a foreign language*\n\nThe `lg` query parameter is used to define the language used on the map tiles. Consult the  Map Tile API Reference for a full list of available languages.\n\n\n\n* **lg**  `enum`\n \\- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0c08e0e5-d036-4ac8-abb4-9a13af6e3b31"
            }
          ]
        }
      ]
    }
  ]
}
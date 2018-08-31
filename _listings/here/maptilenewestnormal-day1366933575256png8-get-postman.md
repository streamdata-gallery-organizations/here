{
  "info": {
    "name": "HERE Map Tile API Support for Multiple Languages",
    "_postman_id": "8ac4426f-0b8e-4814-8dc6-fbc509e264d7",
    "description": "*Request a map tile with labels in two languages*\n\nThe `lg` query parameter is used to define the first language used on the map tiles. The `lg2` query parameter is used to define a supplementary second language. Consult the  Map Tile API Reference for a full list of available languages.\n\n\n\n* **lg**  `enum`\n \\- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **lg2**  `enum`\n \\- Alters the second language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Terrain",
      "item": [
        {
          "id": "e733cfb9-6ec0-4edf-9999-c1cf29909346",
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
              "id": "cc8a14c9-618a-436f-894c-d6e64a36503b"
            }
          ]
        }
      ]
    },
    {
      "name": "Multiple",
      "item": [
        {
          "id": "b209cc5f-a74f-4de4-bafc-7facc118cc43",
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
              "id": "879ac3c2-dc55-4693-8b71-b12cabcc40f1"
            }
          ]
        }
      ]
    },
    {
      "name": "Color-reduced",
      "item": [
        {
          "id": "a93616e7-4380-48ba-8e06-84fa3dd1555d",
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
              "id": "107b6de6-e0ab-4315-851c-142aeb48ccab"
            }
          ]
        }
      ]
    },
    {
      "name": "Filtering",
      "item": [
        {
          "id": "e3790ca0-021b-44a6-85c7-fdc6fa2cf8d4",
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
              "id": "844eeda0-8ac5-412d-8160-7e96c0603c30"
            }
          ]
        }
      ]
    },
    {
      "name": "Hybrid",
      "item": [
        {
          "id": "3da61642-6465-4df4-99f2-b50575d230d3",
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
              "id": "d8f070ba-cfbc-434e-8ce1-9a6d3f3cb0ec"
            }
          ]
        }
      ]
    },
    {
      "name": "Truck",
      "item": [
        {
          "id": "42dc7698-ccd5-42bb-a115-5e39d48d4a22",
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
              "id": "940bd825-bb0c-43e7-bdbf-98a071e7c873"
            }
          ]
        }
      ]
    },
    {
      "name": "Toll",
      "item": [
        {
          "id": "afb69fd8-a3dc-4f69-ad2a-e8575735a998",
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
              "id": "cf61d45c-2a7a-4eb5-9305-9f2330bd3cb6"
            }
          ]
        }
      ]
    },
    {
      "name": "Point",
      "item": [
        {
          "id": "fda88b13-72ee-4f39-99c3-1a0b152d786d",
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
              "id": "beba366b-c3d0-43dd-8b0a-1b969431ecae"
            }
          ]
        }
      ]
    },
    {
      "name": "Copyright",
      "item": [
        {
          "id": "df52b5cb-ddb8-46b3-9e7f-cd2029ad7bbb",
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
              "id": "7fb11682-2f74-42a2-9e54-9a1cb3f6b232"
            }
          ]
        }
      ]
    },
    {
      "name": "Satellite",
      "item": [
        {
          "id": "3221e8c3-e7ef-402d-a5e8-0e77e2a4276e",
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
              "id": "9af35d34-35d9-4ef6-80e4-1e3b8f2107cb"
            }
          ]
        }
      ]
    },
    {
      "name": "Foreign",
      "item": [
        {
          "id": "ec672ed7-35f5-4953-afd8-faf7e775a454",
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
              "id": "3b70c71b-9245-499c-a5a3-8006672a1a9c"
            }
          ]
        }
      ]
    },
    {
      "name": "Fleet",
      "item": [
        {
          "id": "cbcdfeef-9ddd-4ddc-839d-3b8d70b86018",
          "name": "MaptileNewestNormalDay1340932723256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/13/4093/2723/256/png8?app_code=%7B%7D&app_id=%7B%7D&style=%7B%7D",
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
            "description": "*Request a street map tile using the fleet vehicle color scheme*\n\nFleet color scheme map tiles are available by passing `style=fleet` as a parameter of the request URL.\n\n\n\n* **style**  `enum`\n \\- If present, selects the style to use to render the tile.\n\n Valid values are : `default`, `alps`, `fleet`, `wings`, `dreamworks`, `flame`, `mini`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83b11105-d20f-4772-910a-354e555a1429"
            }
          ]
        }
      ]
    },
    {
      "name": "SupportMultiple",
      "item": [
        {
          "id": "ec0b8aeb-b398-4ec0-a7ff-2f576f29008e",
          "name": "MaptileNewestNormalDay1366933575256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/13/6693/3575/256/png8?app_code=%7B%7D&app_id=%7B%7D&lg=%7B%7D&lg2=%7B%7D",
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
            "description": "*Request a map tile with labels in two languages*\n\nThe `lg` query parameter is used to define the first language used on the map tiles. The `lg2` query parameter is used to define a supplementary second language. Consult the  Map Tile API Reference for a full list of available languages.\n\n\n\n* **lg**  `enum`\n \\- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **lg2**  `enum`\n \\- Alters the second language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9f00b493-b62a-4d1f-88b6-4de4a5babfe8"
            }
          ]
        }
      ]
    }
  ]
}
---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Map Tile API Base64 Encoded Map Tile
  description: "*Request a base64 encoded map tile*\n\nBase64 encoded tiles are requested
    by adding the parameter `output=base64` to the request URL.\n  \n  Click on the
    response to decode the tile returned.\n\n\n\n* **output**  `text`\n \\- Indicates
    whether to return the tile as base64 encoded text.\n\n* **app_id**  `text`\n \\-
    A 20 byte Base64 URL-safe encoded string used for the authentication of the client
    application.    You must include an `app_id` with every request.\n\n* **app_code**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_code` with every request."
  version: 1.0.0
host: 1.aerial.maps.cit.api.here.com
basePath: /maptile/2.1/maptile/newest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /terrain.day/7/66/45/256/png8:
    get:
      summary: Terrain Map
      description: |-
        *Request a terrain map tile*

        Terrain map tile are available by passing `terrain.day` in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: TerrainDay76645256Png8Get
      x-api-path-slug: terrain-day76645256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Terrain
      - Map
  /maptile/newest/normal.day/6/30/24/256/png8:
    get:
      summary: Multiple Base64 Encoded Map Tiles
      description: "*Request multiple base64 encoded map tiles*\n\nA square consisting
        of multiple base64 encoded tiles is requested by adding the parameters `output=base64`
        and `range=NxN` to the request URL. The `column` and `row` in the path of
        the URL, defining the top left-hand corner of the tile group must be divisible
        by the value of the `range` parameter.\n  \n  Click on the response to decode
        the tiles returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to
        return the tile as base64 encoded text.\n\n* **range**  `enum`\n \\- Indicates
        the size of the array of tiles returned. Valid values are `2x2`, `3x3` or
        `4x4`\n\n Valid values are : `2x2`, `3x3`, `4x4`\n\n* **app_id**  `text`\n
        \\- A 20 byte Base64 URL-safe encoded string used for the authentication of
        the client application.    You must include an `app_id` with every request.\n\n*
        **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an `app_code`
        with every request."
      operationId: MaptileNewestNormalDay63024256Png8Get
      x-api-path-slug: maptilenewestnormal-day63024256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: output
      - in: query
        name: range
      responses:
        200:
          description: OK
      tags:
      - Multiple
      - Base64
      - Encoded
      - Map
      - Tiles
  /maptile/newest/normal.day.transit/12/2074/1409/256/png8:
    get:
      summary: Color-reduced Transit Map
      description: |-
        *Request a color-reduced map tile with public transport*

        Color-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: MaptileNewestNormalDayTransit1220741409256Png8Get
      x-api-path-slug: maptilenewestnormal-day-transit1220741409256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Color-reduced
      - Transit
      - Map
  /maptile/newest/normal.day/16/18743/25072/256/png8:
    get:
      summary: Filtering Points of Interest
      description: "*Request a map tile including selected points of interest*\n\nPoints
        of interest are displayed by passing the `pois` parameter in the request URL.
        The type of points of interest to be displayed can be filtered by using a
        hexadecimal bitmask.\n  \n\n\n\n* **pois**  `text`\n \\- Displays points of
        interest if present  \n\n Valid values are : `default`, `alps`, `fleet`, `wings`,
        `dreamworks`, `flame`, `mini`\n\n* **app_id**  `text`\n \\- A 20 byte Base64
        URL-safe encoded string used for the authentication of the client application.
        \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
        \\- A 20 byte Base64 URL-safe encoded string used for the authentication of
        the client application.    You must include an `app_code` with every request."
      operationId: MaptileNewestNormalDay161874325072256Png8Get3
      x-api-path-slug: maptilenewestnormal-day161874325072256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: pois
      responses:
        200:
          description: OK
      tags:
      - Filtering
      - Points
      - Of
      - Interest
  /hybrid.day/4/8/5/256/png8:
    get:
      summary: Hybrid Map
      description: |-
        *Request a hybrid map tile - satellite imagery with labels*

        Hybrid map tile are available by passing `hybrid.day` in the path of the request URL. The map tiles will display using the default language of the server unless the `lg` query parameter is used to change the map tile language. Consult the  Map Tile API Reference for a full list of available languages.



        * **lg**  `enum`
         \- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.

         Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: HybridDay485256Png8Get
      x-api-path-slug: hybrid-day485256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lg
      responses:
        200:
          description: OK
      tags:
      - Hybrid
      - Map
  /trucktile/newest/normal.day/12/2199/1342/256/png8:
    get:
      summary: Truck Restrictions Map
      description: |-
        *Request a street map tile showing restrictions for heavy vehicles*

        To obtain a map tile displaying route restrictions for trucks, use the `trucktile` parameter in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: TrucktileNewestNormalDay1221991342256Png8Get
      x-api-path-slug: trucktilenewestnormal-day1221991342256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Truck
      - Restrictions
      - Map
  /maptile/newest/normal.day/9/255/170/256/png8:
    get:
      summary: Toll Zone Map
      description: |-
        *Request a street map tile highlighting congestion and environmental toll zones*

        To highlight such toll zones, add the `congestion` parameter to the request URL.



        * **congestion**  `null`
         \- Flag to indicate if congestion zones are to be shown on the map.

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: MaptileNewestNormalDay9255170256Png8Get
      x-api-path-slug: maptilenewestnormal-day9255170256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: congestion
      responses:
        200:
          description: OK
      tags:
      - Toll
      - Zone
      - Map
  /meta/pois:
    get:
      summary: Point of Interest Categories
      description: "*Request point of interest category information*\n\nTo make a
        request for point-of-interest information, use `meta/pois` in the path of
        the request URL.\n  \n\n\n\n* **output**  `enum`\n \\- A 20 byte Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an `app_id` with every request.\n\n Valid values are : `json`,
        `text`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
        used for the authentication of the client application.    You must include
        an `app_id` with every request..  \n\n* **app_code**  `text`\n \\- A 20 byte
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an `app_code` with every request."
      operationId: MetaPoisGet
      x-api-path-slug: metapois-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: output
      responses:
        200:
          description: OK
      tags:
      - Point
      - Of
      - Interest
      - Categories
  /copyright/newest:
    get:
      summary: Copyright Information
      description: "*Request map tile copyright information*\n\nTo make a request
        for copyright information, use the `copyright` parameter in the path of the
        request URL.\n  \n  Note that the client-side process formatting the JSON
        response may take some time in older browsers.\n\n\n\n* **app_id**  `text`\n
        \\- A 20 byte Base64 URL-safe encoded string used for the authentication of
        the client application.    You must include an `app_id` with every request.\n\n*
        **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an `app_code`
        with every request."
      operationId: CopyrightNewestGet
      x-api-path-slug: copyrightnewest-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Copyright
      - Information
  /satellite.day/5/15/12/256/png8:
    get:
      summary: Satellite Map
      description: |-
        *Request a satellite map tile*

        Satellite map tiles do not display labels and are available by passing `satellite.day` in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: SatelliteDay51512256Png8Get
      x-api-path-slug: satellite-day51512256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Satellite
      - Map
  /maptile/newest/normal.day/11/1196/595/256/png8:
    get:
      summary: Foreign Language Support
      description: |-
        *Request a map tile with labels in a foreign language*

        The `lg` query parameter is used to define the language used on the map tiles. Consult the  Map Tile API Reference for a full list of available languages.



        * **lg**  `enum`
         \- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.

         Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: MaptileNewestNormalDay111196595256Png8Get
      x-api-path-slug: maptilenewestnormal-day111196595256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lg
      responses:
        200:
          description: OK
      tags:
      - Foreign
      - Language
      - Support
  /maptile/newest/normal.day/13/4093/2723/256/png8:
    get:
      summary: Fleet Vehicle Map
      description: |-
        *Request a street map tile using the fleet vehicle color scheme*

        Fleet color scheme map tiles are available by passing `style=fleet` as a parameter of the request URL.



        * **style**  `enum`
         \- If present, selects the style to use to render the tile.

         Valid values are : `default`, `alps`, `fleet`, `wings`, `dreamworks`, `flame`, `mini`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: MaptileNewestNormalDay1340932723256Png8Get
      x-api-path-slug: maptilenewestnormal-day1340932723256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: style
      responses:
        200:
          description: OK
      tags:
      - Fleet
      - Vehicle
      - Map
  /maptile/newest/normal.day/13/6693/3575/256/png8:
    get:
      summary: Support for Multiple Languages
      description: |-
        *Request a map tile with labels in two languages*

        The `lg` query parameter is used to define the first language used on the map tiles. The `lg2` query parameter is used to define a supplementary second language. Consult the  Map Tile API Reference for a full list of available languages.



        * **lg**  `enum`
         \- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.

         Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh

        * **lg2**  `enum`
         \- Alters the second language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.

         Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: MaptileNewestNormalDay1366933575256Png8Get
      x-api-path-slug: maptilenewestnormal-day1366933575256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lg
      - in: query
        name: lg2
      responses:
        200:
          description: OK
      tags:
      - SupportMultiple
      - Languages
  /maptile/newest/normal.day/11/525/761/256/png8:
    get:
      summary: Base64 Encoded Map Tile
      description: "*Request a base64 encoded map tile*\n\nBase64 encoded tiles are
        requested by adding the parameter `output=base64` to the request URL.\n  \n
        \ Click on the response to decode the tile returned.\n\n\n\n* **output**  `text`\n
        \\- Indicates whether to return the tile as base64 encoded text.\n\n* **app_id**
        \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an `app_id` with every request.\n\n*
        **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an `app_code`
        with every request."
      operationId: MaptileNewestNormalDay11525761256Png8Get4
      x-api-path-slug: maptilenewestnormal-day11525761256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: output
      responses:
        200:
          description: OK
      tags:
      - Base64
      - Encoded
      - Map
      - Tile
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
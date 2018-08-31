---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Public Transit API All Next Departures for a list of Stations
  description: "*Request a list of all next departure times and destinations for a
    give list of stations.*\n\nAll next departures for a list of stations can be requested
    using the `metarouter/rest/boardservice/v1/multiboard/by_stopIds.json` and specifying
    a `time` and `stopIds.`  \nThe maximum numbers of nearby stations and number of
    departures per station can be restricted by using the `max_stn` and `max` parameters,
    respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n*
    **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number
    of next departures per station to be included in the response.     The default
    value is 40.    \n\n* **max_stn**  `text`\n \\-  The maximum number of stations
    for which departures are required.     The default value is 40.    \n\n* **stopIds**
    \ `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId must
    contain\n at least 6 characters and must not exceed a maximum of 1000 characters."
  version: 1.0.0
host: cit.transit.api.here.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /jobs/puwWrv32YOU24y8MNoUr793chFAI36aC:
    get:
      summary: Get Job
      description: "*Request the status of a batch geocoder job*\n\nTo check the status,
        make a request to the `jobs` endpoint  appending the `requestId` and using
        the parameter `action=status `\n  \n\n\n\n* **action**  `enum`\n \\- Type
        of request  \n\n Valid values are : `cancel`, `runs`, `status`\n\n* **app_code**
        \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an `app_code` with every request.
        \ \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
        used for the authentication of the client application.    You must include
        an `app_id` with every request."
      operationId: getJob
      x-api-path-slug: jobspuwwrv32you24y8mnour793chfai36ac-get
      parameters:
      - in: query
        name: action
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Job
  /jobs:
    post:
      summary: Add Jobs
      description: "* Start asynchronously geocoding a large set of addresses in one
        batch*\n\nSubmit an HTTP POST request with `action=run` and attach the input
        data to the body. \n  \n\n\n\n* **gen**  `number`\n \\- Enables/disables backward
        incompatible behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64
        URL-safe encoded string used for the authentication of the client application.
        \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
        \\- A 20 byte Base64 URL-safe encoded string used for the authentication of
        the client application.    You must include an `app_code` with every request.\n\n*
        **action**  `enum`\n \\- Type of request\n\n Valid values are : `cancel`,
        `run`, `status`\n\n* **mailto**  `text`\n \\- Email address where completion
        notification is sent.\n\n* **header**  `enum`\n \\- If `true`, a header row
        is included before the results in the output.  \n\n Valid values are : `false`,
        `true`\n\n* **indelim**  `text`\n \\- \n\n* **outdelim**  `text`\n \\- \n\n*
        **outcols**  `text`\n \\- \n\n* **outputCombined**  `enum`\n \\- \n\n Valid
        values are : `true`, `false`"
      operationId: addJob
      x-api-path-slug: jobs-post
      parameters:
      - in: query
        name: action
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: gen
      - in: query
        name: header
      - in: query
        name: indelim
      - in: query
        name: mailto
      - in: query
        name: outcols
      - in: query
        name: outdelim
      - in: query
        name: outputCombined
      responses:
        200:
          description: OK
      tags:
      - Job
  /bbox:
    get:
      summary: Find Locations within a Bounding Box
      description: |-
        *Request a list of user-defined locations within a defined area*

        The request uses the `bbox` endpoint, and the bounding box is specified by adding the `bbox` parameter to the request URL.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **bbox**  `bbox`
         \- Restricts results to be found within this bounding box

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: BboxGet2
      x-api-path-slug: bbox-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: bbox
      - in: query
        name: layerId
      responses:
        200:
          description: OK
      tags:
      - Find
      - Locations
      - Within
      - Bounding
      - Box
  /attribute:
    get:
      summary: Filtering by Custom Attributes
      description: |-
        *Request a list of user-defined locations based on their attribute values*

        An attribute-based search is requested using the `attribute` endpoint and by adding the `query` parameter to the request URL.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **query**  `text`
         \- The query to retrieve

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: AttributeGet
      x-api-path-slug: attribute-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: layerId
      - in: query
        name: query
      responses:
        200:
          description: OK
      tags:
      - Filtering
      - By
      - Custom
      - Attributes
  /proximity:
    get:
      summary: Find the Five Nearest Locations
      description: |-
        *Request a list of user-defined locations within a circle around a fixed point*

        The search uses the `proximity` endpoint. The definition of the location and limit of the search is specified using  `coord` and `radius` parameters, and the number of results returned limited by adding the `limit` parameter to the request URL.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **coord**  `latlng`
         \- Center of the proximity search

        * **radius**  `number`
         \- width of the search corridor

        * **limit**  `number`
         \- The limit of the number of items contained in the response.

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: ProximityGet2
      x-api-path-slug: proximity-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: coord
      - in: query
        name: layerId
      - in: query
        name: limit
      - in: query
        name: radius
      responses:
        200:
          description: OK
      tags:
      - Find
      - Five
      - Nearest
      - Locations
  /route/corridor:
    get:
      summary: Find Locations along a pre-defined Route
      description: |-
        *Request a list of user-defined locations along a pre-defined route*

        The route has been pre-calculated and the `routeid` has already been acquired from a previous routing request. A route-based corridor search is requested using the `corridor` endpoint and by adding the `routeid` parameter to the request URL, along with a corridor `width`.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **routeId**  `text`
         \- A <b>previously</b> calculated routeId

        * **radius**  `number`
         \- Width of the search corridor

        * **limit**  `number`
         \- The limit of the number of items contained in the response.

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: RouteCorridorGet
      x-api-path-slug: routecorridor-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: layerId
      - in: query
        name: limit
      - in: query
        name: radius
      - in: query
        name: routeId
      responses:
        200:
          description: OK
      tags:
      - Find
      - Locations
      - Along
      - Pre-defined
      - Route
  /corridor:
    get:
      summary: Find Locations using Corridor
      description: |-
        *Request a list of user-defined locations near to a given corridor*

        The route corridor consists of a series of latitude, longitude pairs defining the waypoints of a route, along with a defined width. A corridor search is requested using the `corridor` endpoint and by adding a series of comma delimited latitude, longitude waypoints to the `route` parameter of the request URL, along with a `radius` for the search.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **route**  `text`
         \- A type of spatial filter. The corridor is defined by its path and width. The path is a line along the center of the corridor represented by a series of latitude/longitude pairs. Corridor width is given in meters.

        * **radius**  `number`
         \- width of the search corridor

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: CorridorGet
      x-api-path-slug: corridor-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: layerId
      - in: query
        name: radius
      - in: query
        name: route
      responses:
        200:
          description: OK
      tags:
      - Find
      - Locations
      - Using
      - Corridor
  /geocode.json:
    get:
      summary: Geocode using partial address information
      description: "*Request the latitude, longitude and details of an address based
        on partial address information*\n\nThis example shows a structured (qualified)
        geocoding request using the `geocode` endpoint. In this structured request
        the data is provided in `country`, `city`, `street` and `housenumber` parameters
        in the request URL. Note that the street name misses the directional (\"W\")
        and also the street type. The omitted directional makes the query ambiguous
        and the response contains therefore two results: One address on West Randolph
        St and one on East Randolph St.\n  \n\n\n\n* **housenumber**  `text`\n \\-
        The house number or house name\n\n* **street**  `text`\n \\- The street name
        can include suite, apt and floor information.\n\n* **city**  `text`\n \\-
        City name\n\n* **country**  `text`\n \\- Specify the country or list of countries
        using the country code (3 bytes, ISO 3166-1-alpha-3) or the country name\n\n*
        **gen**  `number`\n \\- Enables/disables backward incompatible behavior in
        the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
        used for the authentication of the client application.    You must include
        an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an `app_code` with every request."
      operationId: GeocodeJsonGet5
      x-api-path-slug: geocode-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: city
      - in: query
        name: country
      - in: query
        name: gen
      - in: query
        name: housenumber
      - in: query
        name: street
      responses:
        200:
          description: OK
      tags:
      - Geocode
      - Using
      - Partial
      - Address
      - Information
  /reversegeocode.json:
    get:
      summary: Reverse Geocode Landmarks
      description: |-
        *Request details of landmarks near to a given latitude and longitude*

        Landmark reverse geocoding requests can be made using the `reversegeocode` endpoint, specifying the parameter `mode=retrieveLandmarks`, and adding the `prox` parameter to the request URL.  Consult the  Geocoder API Reference for a full list of available landmark types.



        * **prox**  `prox`
         \- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`

        * **mode**  `enum`
         \- Type of search invoked. Search for streets, administrative areas or landmarks, or a combination of all three

         Valid values are : `retrieveAddresses`, `retrieveAreas`, `retrieveLandmarks`, `retrieveAll`, `trackPosition`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **gen**  `number`
         \- Enables/disables backward incompatible behavior in the API
      operationId: ReversegeocodeJsonGet4
      x-api-path-slug: reversegeocode-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: gen
      - in: query
        name: mode
      - in: query
        name: prox
      responses:
        200:
          description: OK
      tags:
      - Reverse
      - Geocode
      - Landmarks
  /multi-reversegeocode.json:
    post:
      summary: Multi-reverse Geocode Addresses
      description: "*Request the addresses of up to one hundred locations with one
        multi-reverse geocoding request*\n\nThe body of the HTTP POST request contains
        the coordinates and optional radius in the `prox` parameter and an optional
        numeric identifier in the `id` parameter as plain text, one line per pair
        of coordinates. The identifier associates each result with the corresponding
        input. If no id is provided the system creates one starting with 0.\n  \n\n\n\n*
        **mode**  `enum`\n \\- Search for prominent landmarks nearby  \n\n Valid values
        are : `retrieveAddresses`, `retrieveAreas`, `retrieveLandmarks`, `retrieveAll`,
        `trackPosition`\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible
        behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\-
        A 20 byte Base64 URL-safe encoded string used for the authentication of the
        client application.    You must include an `app_code` with every request.\n\n*
        **Content-Type**  `header`\n\n  Accept any content in return\n\n* **Cache-Control**
        \ `header`\n\n  Ensure that the request is always passed to server so that
        latest response is retrieved"
      operationId: MultiReversegeocodeJsonPost2
      x-api-path-slug: multireversegeocode-json-post
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: header
        name: Cache-Control
      - in: header
        name: Content-Type
      - in: query
        name: gen
      - in: query
        name: mode
      responses:
        200:
          description: OK
      tags:
      - Multi-reverse
      - Geocode
      - Resses
  /mapview:
    get:
      summary: Map Image using Bounding Box
      description: |-
        *Request an image of a map based around a given area*

        To specify a bounding box, add the `bbox` parameter to the request URL. On desktop browsers, redirection to `here.com` will occur automatically unless the `nord` parameter is also added to URL.



        * **bbox**  `text`
         \- Bounding box of the map specifying the top-right and bottom left corners.    e.g. `52.515,13.377,52.134,13.978`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: MapviewGet15
      x-api-path-slug: mapview-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: bbox
      responses:
        200:
          description: OK
      tags:
      - Map
      - Image
      - Using
      - Bounding
      - Box
  /route:
    get:
      summary: Map Image with Polylines
      description: "*Request an image of a map including a polyline*\n\nIt supports
        also different map schemes, image sizes; image formats as \r\nwell as zooming
        out from automatically calculated zoom level.\n  \n\n\n\n* **r0**  `text`\n
        \\- List of coordinates describing the first route\n\n* **r1**  `text`\n \\-
        List of coordinates describing the second route\n\n* **m0**  `text`\n \\-
        First route marker on the map\n\n* **m1**  `text`\n \\- Second route marker
        on the map\n\n* **lc0**  `text`\n \\- Color of the first route line displayed
        on the map\n\n* **sc0**  `text`\n \\- Shadow color of the first route line
        displayed on the map\n\n* **lw0**  `number`\n \\- Width of the first route
        line displayed on the map\n\n* **lc1**  `text`\n \\- Color of the second route
        line displayed on the map\n\n* **sc1**  `text`\n \\- Shadow color of the second
        route line displayed on the map\n\n* **lw1**  `number`\n \\- Width of the
        second route line displayed on the map\n\n* **w**  `number`\n \\- Image width
        in pixels, maximum 2048.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\-
        A 20 byte Base64 URL-safe encoded string used for the authentication of the
        client application.    You must include an `app_code` with every request."
      operationId: RouteGet
      x-api-path-slug: route-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lc0
      - in: query
        name: lc1
      - in: query
        name: lw0
      - in: query
        name: lw1
      - in: query
        name: m0
      - in: query
        name: m1
      - in: query
        name: r0
      - in: query
        name: r1
      - in: query
        name: sc0
      - in: query
        name: sc1
      - in: query
        name: w
      responses:
        200:
          description: OK
      tags:
      - Map
      - Image
      - Polylines
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
  /maptile/newest/normal.day.grey/11/525/761/256/png8:
    get:
      summary: Color-reduced Street Map
      description: |-
        *Request a greyed out street map tile*

        Maps using a reduced color palette can be requested by passing `normal.day.grey` in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: MaptileNewestNormalDayGrey11525761256Png8Get
      x-api-path-slug: maptilenewestnormal-day-grey11525761256png8-get
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
      - Street
      - Map
  /info:
    get:
      summary: Map Tile Type Information
      description: |-
        *Request information about the types of map tiles available on a server*

        To make a request for metadata information, use the `info` parameter in the path of the request URL.



        * **output**  `enum`
         \- Indicates whether to return the information in XML format, JSON format or as an XML schema (XSD) of the API metadata

         Valid values are : `json`, `xml`, `xsd`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: InfoGet
      x-api-path-slug: info-get
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
      - Map
      - Tile
      - Type
      - Information
  /truckonlytile/newest/normal.day/12/2199/1342/256/png8:
    get:
      summary: Transparent Truck Restrictions Map
      description: |-
        *Request a transparent tile showing restrictions for heavy vehicles only*

        To obtain a transparent map tile displaying route restrictions for trucks, use the `truckonlytile` parameter in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: TruckonlytileNewestNormalDay1221991342256Png8Get
      x-api-path-slug: truckonlytilenewestnormal-day1221991342256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Transparent
      - Truck
      - Restrictions
      - Map
  /suggest:
    get:
      summary: Search Suggestions
      description: |-
        *Request a list of suggestions based on a partial query string*

        A suggestions request can be made using the `suggest` endpoint in the request URL and adding the `q` parameter with the partial query string. The focal point for the suggestion service is defined using the `at` parameter.



        * **at**  `latlng`
         \- Location of the central point for the places search.    e.g. `52.515,13.377`

        * **q**  `text`
         \- Free-form text containing the search term.    e.g. `restaurant` or `Brandenburger Tor`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Accept**  `header`

          Format to request from the server
      operationId: SuggestGet
      x-api-path-slug: suggest-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: at
      - in: query
        name: q
      responses:
        200:
          description: OK
      tags:
      - Search
      - Suggestions
  /categories/places:
    get:
      summary: Place Categories
      description: |-
        *Request a list of place categories available for a given location*

        A place category request can be made using the `categories/places` endpoint in the request URL and specifying the  focal point using the `at` parameter.



        * **at**  `latlng`
         \- Location of the central point for the places search.    e.g. `52.515,13.377`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Accept**  `header`

          Format to request from the server
      operationId: CategoriesPlacesGet
      x-api-path-slug: categoriesplaces-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: at
      responses:
        200:
          description: OK
      tags:
      - Place
      - Categories
  /discover/explore:
    get:
      summary: Explore Popular Places
      description: |-
        *Request a list of popular places around a location*

        The `explore` location context can either be an explicitly given location using the `at` parameter, or implicitly defined by a user's current position or the currently visible map.



        * **at**  `latlng`
         \- Location of the central point for the places search.    e.g. `52.515,13.377`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Accept**  `header`

          Format to request from the server
      operationId: DiscoverExploreGet5
      x-api-path-slug: discoverexplore-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: at
      responses:
        200:
          description: OK
      tags:
      - Explore
      - Popular
      - Places
  /discover/here:
    get:
      summary: Explore Nearby Places
      description: |-
        *Request a list of places close to a location *

        The `discover/here` endpoint allow users to request a list of places near to a given point, based on a location precision parameter (in this case the `at` parameter) which must be provided. If the precision is high, the places around that point are returned in order of proximity. Otherwise a set of recommended places in the area is returned.



        * **at**  `latlng`
         \- Location of the central point for the places search.    e.g. `52.515,13.377`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Accept**  `header`

          Format to request from the server
      operationId: DiscoverHereGet
      x-api-path-slug: discoverhere-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: at
      responses:
        200:
          description: OK
      tags:
      - Explore
      - Nearby
      - Places
  /discover/search:
    get:
      summary: One-Box Search
      description: |-
        *Request a list of nearby places based on a query string*

        A free-text places search can be made using the `discover/search` endpoint in the request URL and adding the `q` parameter with the query string. The focal point of the search is defined using the `at` parameter.



        * **at**  `latlng`
         \- Location of the central point for the places search.    e.g. `52.515,13.377`

        * **q**  `text`
         \- Free-form text containing the search term.    e.g. `restaurant` or `Brandenburger Tor`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Accept**  `header`

          Format to request from the server
      operationId: DiscoverSearchGet
      x-api-path-slug: discoversearch-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: at
      - in: query
        name: q
      responses:
        200:
          description: OK
      tags:
      - One-Box
      - Search
  /search/by_name.json:
    get:
      summary: Find Stations by Name
      description: "*Request a list of public transit stations based on name*\n\nA
        station search request can be made using the `search/by_name.json` endpoint
        and adding the `name` parameter. The focal point of the search is defined
        using the `x` and `y` parameters. The number of results can be further restricted
        by `max `and the `radius `parameters.\n  \n\n\n\n* **x**  `number`\n \\- The
        longitude of the center point of your search.    e.g. `13.377`\n\n* **y**
        \ `number`\n \\- The latitude of the center point of your search.    e.g.
        `52.515`\n\n* **name**  `text`\n \\- Specifies the name or a part of the name
        of the station to search for and can be one word, multiple words or partial
        word separated by either comma or space.\n\n* **app_id**  `text`\n \\- A 20
        bytes Base64 URL-safe encoded string used for the authentication of the client
        application.    You must include an app_code and app_code with every request.\n\n*
        **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used
        for the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the
        maximum number of stations/stops included in the response.\n  The minimum
        value is 1 and the maximum value is not limited.\n  The default value is 5.
        \    \n\n* **method**  `enum`\n \\- Specifies if the matching method is *fuzzy*
        or *strict*.\n  The default value is *fuzzy*.\n    * fuzzy - search for stations
        with the name having similar sounding and/or similar spelling to the names
        requested\n    * strict - search for stations with the name exactly matching
        the names requested or contains it as its part.\n\n   Valid values are : `fuzzy`,
        `strict`\n\n* **radius**  `number`\n \\- Specifies a radius in meters when
        combined with a center point defines the area of the search. The minimum value
        is 0 and the maximum value is not limited.\n  The default value is 20000km."
      operationId: SearchByNameJsonGet
      x-api-path-slug: searchby-name-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: max
      - in: query
        name: method
      - in: query
        name: name
      - in: query
        name: radius
      - in: query
        name: x
      - in: query
        name: "y"
      responses:
        200:
          description: OK
      tags:
      - Find
      - Stations
      - By
      - Name
  /metarouter/rest/routeservice/v2/route.json:
    get:
      summary: Avoid Transit Routes Involving Transfers
      description: "*Request a direct public transit route excluding changes and transfers*\n\nPublic
        transit routes can be requested using the `metarouter/rest/routeservice/v2/route.json`
        endpoint. The `changes `parameter is used to indicate the number of changes
        or transfers desired. \n\n\n\n* **startX**  `number`\n \\- The longitude of
        the start point of your journey.    e.g. `13.377`\n\n* **startY**  `number`\n
        \\- The latitude of the start point of your journey.    e.g. `52.515`\n\n*
        **destX**  `number`\n \\- The longitude of the destination point of your journey.
        \   e.g. `13.377`\n\n* **destY**  `number`\n \\- The latitude of the destination
        point of your journey.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in
        format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64
        URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request.\n\n* **app_code**
        \ `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an app_code and app_code with
        every request.\n\n* **routing**  `enum`\n \\- Type of routing response required.
        \ tt: time-table routing, i.e. route response will show scheduled arrival/departure
        times of the transit at the stations.  sr: simple (or estimated) routing,
        i.e. route response will only show \nthe transit journey but without scheduled
        arrival/departure times.  all: for both estimated and time-table routing.
        \ Default: tt  \n\n    Valid values are : `tt`, `sr`, `all`\n\n* **changes**
        \ `enum`\n \\- Maximum number of changes or transfers. \n                Valid
        values: 0-6 or -1. Default: -1 (any number of transfers permitted).\n\n    >**NOTE:**
        In areas where this parameter is not supported the route response will show
        an attribute `sup_changes=0` in the `Connections` node.\n\n    Valid values
        are : `-1`, `0`, `1`, `2`, `3`, `4`, `5`, `6`"
      operationId: MetarouterRestRouteserviceV2RouteJsonGet8
      x-api-path-slug: metarouterrestrouteservicev2route-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: changes
      - in: query
        name: destX
      - in: query
        name: destY
      - in: query
        name: routing
      - in: query
        name: startX
      - in: query
        name: startY
      - in: query
        name: time
      responses:
        200:
          description: OK
      tags:
      - Avoid
      - Transit
      - Routes
      - Involving
      - Transfers
  /isochrone/v1/search.json:
    get:
      summary: Reachability of an Area Within a Specific Time
      description: "*Request a list of the public transit stations that can be reached
        in a given time*\n\nTo find the stations reachable in a specified time use
        the `isochrone/v1/search.json` endpoint specifying a center point using the
        `x` and `y` parameters and a maximum total duration in minutes using the `max_dur
        `parameter.\n  \n\n\n\n* **max_dur**  `number`\n \\- Maximum duration of the
        journeys, in minutes.   Minimum = 5, Maximum = 90.    The default duration
        is 15 minutes.    \n\n* **y**  `number`\n \\- The latitude of the start point
        of your journey.    e.g. `52.515`  \n\n* **x**  `number`\n \\- The longitude
        of the start point of your journey.    e.g. `13.377`    \n\n* **time**  `text`\n
        \\- Specifies the time in ISO 8601 (for example, 2015-10-18T06:36:40)\n        format.
        \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used
        for the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request."
      operationId: IsochroneV1SearchJsonGet2
      x-api-path-slug: isochronev1search-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: max_dur
      - in: query
        name: time
      - in: query
        name: x
      - in: query
        name: "y"
      responses:
        200:
          description: OK
      tags:
      - Reachability
      - Of
      - Area
      - Within
      - Specific
      - Time
  /metarouter/rest/boardservice/v1/multiboard.json:
    get:
      summary: All Next Departures (deprecated)
      description: "*Request a list of all next departure times and destinations from
        a location.*\n\nAll next departures information can be requested using the
        `metarouter/rest/boardservice/v1/multiboard.json` and specifying a `time`
        and `coordinates. `The maximum numbers of nearby stations and number of departures
        per station can be restricted by using the `max_stn` and `max` parameters,
        respectively.\n  \n  <b>NOTE:</b> This API has been deprecated and replaced
        with 2 new endpoints. Please see \n  <b><i>All Next Departures from a Location
        </i></b>and <b><i>All Next Departures for a list of Stations </i></b>for more
        details.\n  \n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n*
        **startX**  `number`\n \\- The longitude of the center point of your search.
        \   e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude of the center
        point of your search.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in
        format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64
        URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request.\n\n* **app_code**
        \ `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an app_code and app_code with
        every request.\n\n* **max**  `text`\n \\- The  maximum number of next departures
        per station to be included in the response.    The default value is 40.  \n\n*
        **max_stn**  `text`\n \\-  The maximum number of stations for which departures
        are required. The default value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit
        binary number, where each bit represents one type of transit.  \n  0: High-speed
        Trains  \n  1: Intercity/EuroCity Trains  \n  2: Inter-regional and fast trains
        \ \n  3: Regional and other trains  \n  4: City trains  \n  5: Buses  \n  6:
        Boat/Ferries  \n  7: Metro/Subway  \n  8: Tram  \n  9: Ordered services/Taxi
        \ \n  10: Inclined/Funicular  \n  11: Aerial/Cable Car  \n  12: Rapid Bus
        \ \n  13: Monorail  \n  14: Air plane  \n  15: Not yet defined  \n  The default
        is 1111111111111111, meaning all supported transit types are permitted."
      operationId: MetarouterRestBoardserviceV1MultiboardJsonGet
      x-api-path-slug: metarouterrestboardservicev1multiboard-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lang
      - in: query
        name: max
      - in: query
        name: max_stn
      - in: query
        name: prod
      - in: query
        name: startX
      - in: query
        name: startY
      - in: query
        name: time
      responses:
        200:
          description: OK
      tags:
      - All
      - Next
      - Departures
      - (deprecated)
  /coverage/v1/nearby.json:
    get:
      summary: Transit Coverage Nearby
      description: "*Request a list of transit operators and station coverage nearby*\n\nOperator
        coverage is requested using the `coverage/v1/nearby.json` endpoint specifying
        the location using the `x` and `y` parameters.\n\n\n\n* **details**  `enum`\n
        \\- Don't show line info in Explored Coverage\n\n    Valid values are : `0`
        - disabled, `1` - enabled\n\n* **y**  `number`\n \\- The latitude of the center
        point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude
        of the center point of your search.    e.g. `13.377`\n\n* **chinaconfig**
        \ `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether
        with results from China.    When enabled, Taiwan will appear as part of China.
        \   \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**
        \ `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an app_code and app_code with
        every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an app_code and app_code with every request."
      operationId: CoverageV1NearbyJsonGet
      x-api-path-slug: coveragev1nearby-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: chinaconfig
      - in: query
        name: details
      - in: query
        name: x
      - in: query
        name: "y"
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Coverage
      - Nearby
  /coverage/v1/search.json:
    get:
      summary: Transit Coverage Within a City
      description: "*Request a list of transit operator coverage within a specified
        city*\n\nA list of operators working within a city is requested using the
        `coverage/v1/search.json` endpoint. The city is specified using the  `q` parameter.\n\n\n\n*
        **q**  `text`\n \\- The name or a part of the name of the city to search.\n\n*
        **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request.\n\n* **max**
        \ `number`\n \\- Maximum number of results to be returned. Default is null.\n\n*
        **details**  `enum`\n \\- With this value set to 1, the list of supported
        operators and population of the city is returned.   When the value is set
        to 0, only the list of matching city names will be returned.  Default value
        = 1\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **chinaconfig**
        \ `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether
        with results from China.      \n\n    Valid values are : `0` - disabled, `1`
        - enabled\n\n* **lang**  `text`\n \\- The language of the response. The value
        complies with the ISO 639-1 standard and defaults to <i>en</i>."
      operationId: CoverageV1SearchJsonGet
      x-api-path-slug: coveragev1search-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: chinaconfig
      - in: query
        name: details
      - in: query
        name: lang
      - in: query
        name: max
      - in: query
        name: q
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Coverage
      - Within
      - City
  /search/by_stopids.json:
    get:
      summary: Find Stations by ID
      description: "*Request details of a specific transit station based on a previous
        request*\n\nStation details are requested using the `search/by_stopids.json`
        endpoint and appending a comma delimited list of `stop-ids` to the request
        URL. Usually, the request to this endpoint will be called after making a station
        search request, to obtain a list of stations Ids.\n  \n\n\n\n* **stopIds**
        \ `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId
        must contain at least 6 characters and must not exceed a maximum of 1000 characters.
        \    The format of a station Id is 123456789#100. Only the first 9-digits
        are mandatory and if the full Id is to be used, the `#` character must be
        encoded as `%23`.      \n\n* **lang**  `text`\n \\- A language of the response.
        \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used
        for the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request."
      operationId: SearchByStopidsJsonGet
      x-api-path-slug: searchby-stopids-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lang
      - in: query
        name: stopIds
      responses:
        200:
          description: OK
      tags:
      - Find
      - Stations
      - By
      - ID
  /search/by_geocoord.json:
    get:
      summary: Find Stations Nearby
      description: "*Request a list of public transit stations within a given geo-location.*\n\nTo
        find the nearest stations use the `search/by_geocoord.json` endpoint specifying
        a center point using the `x` and `y` parameters and a search radius in meters
        using the `radius` parameter. `Max` value can also be used to restrict the
        number of results shown in the response.\n\n\n\n* **y**  `number`\n \\- The
        latitude of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n
        \\- The longitude of the center point of your search.    e.g. `13.377`\n\n*
        **radius**  `number`\n \\- Specifies a radius in meters when combined with
        the geo-coordinates defines the area of the search. The default value is 500m.\n\n*
        **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request.\n\n* **max**
        \ `number`\n \\- Specifies the maximum number of stations/stops included in
        the response. \n          The default value is 5. The minimum value is 1 and
        the maximum value is not limited."
      operationId: SearchByGeocoordJsonGet
      x-api-path-slug: searchby-geocoord-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: max
      - in: query
        name: radius
      - in: query
        name: x
      - in: query
        name: "y"
      responses:
        200:
          description: OK
      tags:
      - Find
      - Stations
      - Nearby
  /coverage/v1/city.json:
    get:
      summary: Find Transit Coverage in Cities Nearby
      description: "*Request a list of transit operators available in cities nearby*\n\nCity
        coverage can be found using the `coverage/v1/city.json` endpoint. The `x`
        and `y` parameters specify the location of the search.\n  The response also
        includes the number of transit lines and transit stops available for each
        city.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center point
        of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude of
        the center point of your search.    e.g. `52.515`\n\n* **chinaconfig**  `enum`\n
        \\- A switch that allows grouping results from Taiwan\ntogether with results
        from China.    When enabled, Taiwan will appear as part of China.    \n\n
        \   Valid values are : `0` - disabled, `1` - enabled\n\n* **radius**  `number`\n
        \\- Specifies a radius in meters when combined with a center point defines
        the area of the search.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an app_code and app_code with every request.\n\n* **app_code**
        \ `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an app_code and app_code with
        every request."
      operationId: CoverageV1CityJsonGet
      x-api-path-slug: coveragev1city-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: chinaconfig
      - in: query
        name: radius
      - in: query
        name: x
      - in: query
        name: "y"
      responses:
        200:
          description: OK
      tags:
      - Find
      - Transit
      - Coverage
      - In
      - Cities
      - Nearby
  /metarouter/rest/boardservice/v2/stationboard.json:
    get:
      summary: Next Nearby Departures from a Station
      description: "*Request a list of next departure times and destinations of a
        particular station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
        and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be
        obtained from making a prior call to one of the station search (by name or
        by geo-coordinates) endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of
        the response\n\n* **stnId**  `number`\n \\- Station Id.  The format of a station
        Id is 123456789#100. Only the first 9-digits are mandatory and if the full
        Id is to be used, the `#` character must be encoded as `%23`.      \n\n* **time**
        \ `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **strict**  `enum`\n
        \\- When `strict=1` the board will include only departures from the given
        station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**
        \ `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an app_code and app_code with
        every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an app_code and app_code with every request."
      operationId: MetarouterRestBoardserviceV2StationboardJsonGet
      x-api-path-slug: metarouterrestboardservicev2stationboard-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lang
      - in: query
        name: stnId
      - in: query
        name: strict
      - in: query
        name: time
      responses:
        200:
          description: OK
      tags:
      - Next
      - Nearby
      - Departures
      - From
      - Station
  /metarouter/rest/boardservice/v1/multiboard/by_stopids.json:
    get:
      summary: All Next Departures for a list of Stations
      description: "*Request a list of all next departure times and destinations for
        a give list of stations.*\n\nAll next departures for a list of stations can
        be requested using the `metarouter/rest/boardservice/v1/multiboard/by_stopIds.json`
        and specifying a `time` and `stopIds.`  \nThe maximum numbers of nearby stations
        and number of departures per station can be restricted by using the `max_stn`
        and `max` parameters, respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language
        of the response\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
        **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request.\n\n* **max**
        \ `text`\n \\- The  maximum number of next departures per station to be included
        in the response.     The default value is 40.    \n\n* **max_stn**  `text`\n
        \\-  The maximum number of stations for which departures are required.     The
        default value is 40.    \n\n* **stopIds**  `text`\n \\- Specifies a list of
        stopIds separated by comma. Each stopId must contain\n at least 6 characters
        and must not exceed a maximum of 1000 characters."
      operationId: MetarouterRestBoardserviceV1MultiboardByStopidsJsonGet
      x-api-path-slug: metarouterrestboardservicev1multiboardby-stopids-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lang
      - in: query
        name: max
      - in: query
        name: max_stn
      - in: query
        name: stopIds
      - in: query
        name: time
      responses:
        200:
          description: OK
      tags:
      - All
      - Next
      - Departuresa
      - List
      - Of
      - Stations
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
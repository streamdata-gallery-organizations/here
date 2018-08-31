---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Waypoint Sequence Extension API Waypoint Sequence for Hazardous Materials
  description: |-
    *Request an ordered list of destinations for a truck carrying hazardous materials*

    Waypoint sequence calcuations are made using the `findsequence` endpoint and appending  `start` and `end` parameters and consecutively numbered `destination` parameters are used to add intermediate points  to the request. Hazardous material types are added as a comma-delimited list to the  `shippedHazardousGoods` parameter. The list of values is defined in the Enterprise Routing API



    * **start**  `latlng`
     \- Start point for the route calculations.    e.g. `52.515,13.377`

    * **destination1**  `latlng`
     \- A point through which the route must pass.    e.g. `52.6172,13.3833`

    * **destination2**  `latlng`
     \- A point through which the route must pass.    e.g. `52.6172,13.3833`

    * **destination3**  `latlng`
     \- A point through which the route must pass.    e.g. `52.6172,13.3833`

    * **destination4**  `latlng`
     \- A point through which the route must pass.    e.g. `52.6172,13.3833`

    * **end**  `latlng`
     \- End point for the route calculations.    e.g. `50.121,8.925`

    * **improveFor**  `enum`
     \- Whether to improve for time or distance

     Valid values are : `time`, `distance`

    * **mode**  `text`
     \- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled`

    * **shippedHazardousGoods**  `multi-enum`
     \- Truck routing only, list of hazardous materials in the vehicle.

     Valid values are : `combustible`, `corrosive`, `explosive`, `flammable`, `gas`, `harmfulToWater`, `organic`, `other`, `poison`, `poisonousInhalation`, `radioActive`

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  version: 1.0.0
host: wse.cit.api.here.com
basePath: /2
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
  /metarouter/rest/boardservice/v1/multiboard/by_geocoord.json:
    get:
      summary: All Next Departures from a Location
      description: "*Request a list of all next departure times and destinations from
        a given location.*\n\nAll next departures from a given location can be requested
        using the `metarouter/rest/boardservice/v1/multiboard/by_geocoord.json` and
        specifying a `time` and `coordinates. `The maximum numbers of nearby stations
        and number of departures per station can be restricted by using the `max_stn`
        and `max` parameters, respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language
        of the response\n\n* **startX**  `number`\n \\- The longitude of the center
        point of your search.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The
        latitude of the center point of your search.    e.g. `52.515`\n\n* **time**
        \ `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n
        \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an app_code and app_code with
        every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an app_code and app_code with every request.\n\n* **max**  `text`\n
        \\- The  maximum number of next departures per station to be included in the
        response.     The default value is 40.  \n\n* **max_stn**  `text`\n \\-  The
        maximum number of stations for which departures are required.     The default
        value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit binary number, where
        each bit represents one type of transit.  \n  0: High-speed Trains  \n  1:
        Intercity/EuroCity Trains  \n  2: Inter-regional and fast trains  \n  3: Regional
        and other trains  \n  4: City trains  \n  5: Buses  \n  6: Boat/Ferries  \n
        \ 7: Metro/Subway  \n  8: Tram  \n  9: Ordered services/Taxi  \n  10: Inclined/Funicular
        \ \n  11: Aerial/Cable Car  \n  12: Rapid Bus  \n  13: Monorail  \n  14: Air
        plane  \n  15: Not yet defined  \n  The default is 1111111111111111, meaning
        all supported transit types are permitted."
      operationId: MetarouterRestBoardserviceV1MultiboardByGeocoordJsonGet
      x-api-path-slug: metarouterrestboardservicev1multiboardby-geocoord-json-get
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
      - From
      - Location
  /static.json:
    get:
      summary: Platform Static Data
      description: |-
        *Request enumerated content from a static data table*

        To request static data use the static.json endpoint and provide the name of the data table using the `content` parameter



        * **region**  `text`
         \- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`

        * **release**  `text`
         \- Map release quarter    e.g. `2014Q4` or `LATEST`

        * **content**  `text`
         \- The name of the static content table requested

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: StaticJsonGet
      x-api-path-slug: static-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: content
      - in: query
        name: region
      - in: query
        name: release
      responses:
        200:
          description: OK
      tags:
      - Platform
      - Static
      - Data
  /doc/layers.json:
    get:
      summary: Available Map Data Layers
      description: |-
        *Request which data layers can be accessed within a specified map region and release*

        To make a request for data layer availability information, use the `layers.json` endpoint, supplying the `release` and `region` parameters.



        * **region**  `text`
         \- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`

        * **release**  `text`
         \- Map release quarter    e.g. `2014Q4` or `LATEST`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: DocLayersJsonGet
      x-api-path-slug: doclayers-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: region
      - in: query
        name: release
      responses:
        200:
          description: OK
      tags:
      - Available
      - Map
      - Data
      - Layers
  /tile.json:
    get:
      summary: Platform Data
      description: |-
        *Request data from a specific data layer about a specified location*

        To request data  from a specified data layer, use the t`ile.json` endpoint, and include the `region`, `release` and `layer` parameters. The area covered is specified by the `level`, `tilex` and `tiley` parameters



        * **region**  `text`
         \- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`

        * **release**  `text`
         \- Map release quarter    e.g. `2014Q4` or `LATEST`

        * **layer**  `text`
         \- Thematic layer

        * **level**  `text`
         \- Specifies the size of the requested tile

        * **tilex**  `text`
         \- Specifies the tile number in West-East direction. This depends on the level.

        * **tiley**  `text`
         \- Specifies the tile number in South-North direction. This depends on the level.

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: TileJsonGet
      x-api-path-slug: tile-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: layer
      - in: query
        name: level
      - in: query
        name: region
      - in: query
        name: release
      - in: query
        name: tilex
      - in: query
        name: tiley
      responses:
        200:
          description: OK
      tags:
      - Platform
      - Data
  /doc/attributes.json:
    get:
      summary: Available Attributes
      description: "*Request which map data layers contain which attributes*\n\nTo
        make a request for map data layer information, use the `attributes``.json`
        endpoint, supplying the `release` and `region` parameters.\n  \n\n\n\n* **region**
        \ `text`\n \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**
        \ `text`\n \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **app_id**
        \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an `app_id` with every request.\n\n*
        **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an `app_code`
        with every request."
      operationId: DocAttributesJsonGet
      x-api-path-slug: docattributes-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: region
      - in: query
        name: release
      responses:
        200:
          description: OK
      tags:
      - Available
      - Attributes
  /doc/maps.json:
    get:
      summary: Map Data Availability and Freshness
      description: |-
        *Request the release date and area covered by each available map region*

        To make a request for release date information, use the `maps.json` endpoint.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: DocMapsJsonGet
      x-api-path-slug: docmaps-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Map
      - Data
      - Availability
      - Freshness
  /doc/layer.json:
    get:
      summary: Available Attributes within a Map Data Layer
      description: |-
        *Request which attributes are available within a specified map data layer*

        To make a request for map data layer information, use the `layer``.json` endpoint, supplying the `release`, `layer` and `region` parameters.



        * **region**  `text`
         \- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`

        * **release**  `text`
         \- Map release quarter    e.g. `2014Q4` or `LATEST`

        * **layer**  `text`
         \- Thematic layer

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: DocLayerJsonGet
      x-api-path-slug: doclayer-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: layer
      - in: query
        name: region
      - in: query
        name: release
      responses:
        200:
          description: OK
      tags:
      - Available
      - Attributes
      - Within
      - Map
      - Data
      - Layer
  /calculateroute.json:
    get:
      summary: Avoid motorways
      description: |-
        *Request a route preferring or avoiding specific types of road*

        Routing preferences can be added by extending the `mode` parameter of the request URL by adding a semi-colon delimited list of route link flags. In this case the addition of `motorway:-3` to the `mode` parameter indicates a strict exclusion of motorways. Consult the Routing API Reference for a full description of `mode` parameter and different feature weights.



        * **waypoint0**  `latlng`
         \- Start point of the route.    e.g. `52.515,13.377`

        * **waypoint1**  `latlng`
         \- Second point through which the route must pass.    e.g. `52.6172,13.3833`

        * **mode**  `text`
         \- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: CalculaterouteJsonGet22
      x-api-path-slug: calculateroute-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: mode
      - in: query
        name: waypoint0
      - in: query
        name: waypoint1
      responses:
        200:
          description: OK
      tags:
      - Avoid
      - Motorways
  /calculatematrix.json:
    get:
      summary: Many to many matrix routing
      description: "*Matrix routing request with three start points and five destinations*\n\nMatrix
        calculations are made using the `calculatematrix` endpoint and appending a
        three start parameters (`start0, ``start1, ``start2)` and multiple consecutively
        numbered `destination` parameters to the request.\n  \n\n\n\n* **start0**
        \ `latlng`\n \\- First start point for the route calculations.    e.g. `52.515,13.377`
        \ \n\n* **start1**  `latlng`\n \\- Second start point for the route calculations.
        \   e.g. `52.515,13.377`  \n\n* **start2**  `latlng`\n \\- Third start point
        for the route calculations.    e.g. `52.515,13.377`  \n\n* **destination0**
        \ `latlng`\n \\- First destination point for the route calculations.    e.g.
        `52.4,13.5`  \n\n* **destination1**  `latlng`\n \\- Second destination point
        for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination2**  `latlng`\n
        \\- Third destination point for the route calculations.    e.g. `52.4,13.5`
        \ \n\n* **destination3**  `latlng`\n \\- Fourth destination point for the
        route calculations.    e.g. `52.4,13.5`    \n\n* **destination4**  `latlng`\n
        \\- Fifth destination point for the route calculations.    e.g. `52.4,13.5`
        \ \n\n* **mode**  `text`\n \\- Routing mode determines how the route is calculated.
        \   e.g. `fastest;car;traffic:disabled.`  \n\n* **app_id**  `text`\n \\- A
        20 byte Base64 URL-safe encoded string used for the authentication of the
        client application.    You must include an app_id with every request.    \n\n*
        **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an app_code
        with every request."
      operationId: CalculatematrixJsonGet2
      x-api-path-slug: calculatematrix-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: destination0
      - in: query
        name: destination1
      - in: query
        name: destination2
      - in: query
        name: destination3
      - in: query
        name: destination4
      - in: query
        name: mode
      - in: query
        name: start0
      - in: query
        name: start1
      - in: query
        name: start2
      responses:
        200:
          description: OK
      tags:
      - Many
      - To
      - Many
      - Matrix
      - Routing
  /calculateisoline.json:
    get:
      summary: Time-based isoline with destination as center
      description: "*Request an isoline that will reach a destination within a given
        time*\n\nTime-based reverse flow requests are made using the `calculateisoline`
        endpoint and specifying the `destination` and `rangetype=time` parameters.\n\n\n\n*
        **mode**  `text`\n \\- Routing mode determines how the route is calculated.
        \   e.g. `fastest;car;traffic:disabled.`\n\n* **destination**  `latlng`\n
        \\- Destination of the reverse flow calculation.    e.g. `52.515,13.377`\n\n*
        **rangetype**  `text`\n \\- Specifies type of range. Possible values are distance,
        time. For distance the unit is  meters. For time the unit is seconds.  rangetype=distance
        \ rangetype=time    \n\n* **range**  `number`\n \\- Range of isoline. Several
        comma separated values can be specified. The unit is defined by  parameter
        rangetype  range=1000  range=1000,2000,3000  \n\n* **app_id**  `text`\n \\-
        A 20 byte Base64 URL-safe encoded string used for the authentication of the
        client application.    You must include an `app_id` with every request.  \n\n*
        **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an `app_code`
        with every request."
      operationId: CalculateisolineJsonGet4
      x-api-path-slug: calculateisoline-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: destination
      - in: query
        name: mode
      - in: query
        name: range
      - in: query
        name: rangetype
      responses:
        200:
          description: OK
      tags:
      - Time-based
      - Isoline
      - Destination
      - As
      - Center
  /getlinkinfo.json:
    get:
      summary: Link Information using linkId
      description: "*Request detailed information about a path segment in the routing
        network given a linkid*\n\nLink information can be retrieved using the `getlinkinfo`
        endpoint, by specifying one or more comma separated linkIds using the `linkids`
        parameter. The `linkids` have been generated from a previous request. Note
        that positive direction '+' in link Ids has to be URL encoded.\n  \n  \n\n\n\n*
        **linkids**  `text`\n \\- Link identifiers for which the detailed information
        is being requested.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\-
        A 20 byte Base64 URL-safe encoded string used for the authentication of the
        client application.    You must include an `app_code` with every request."
      operationId: GetlinkinfoJsonGet2
      x-api-path-slug: getlinkinfo-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: linkids
      responses:
        200:
          description: OK
      tags:
      - Link
      - Information
      - Using
      - LinkId
  /getroute.json:
    get:
      summary: Previously calculated route information
      description: "*Request information about a previously calculated route*\n\nPrevious
        routes can be retrieved using the `getroute` endpoint and appending a `routeid`
        to the request. The `routeid` in question has been generated from a previous
        request. Note that server map updates usually invalidates `routeid` value
        computed on previous map versions. If it is the case, the `routeid` computation
        should be requested again on the map in current  use.\n  \n\n\n\n* **mode**
        \ `text`\n \\- Routing mode determines how the route is calculated.    e.g.
        `fastest;car;traffic:disabled.`  \n\n* **routeid**  `text`\n \\- Route identifier
        for which the detailed route information is being requested.  \n\n* **app_id**
        \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an `app_id` with every request.
        \ \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
        used for the authentication of the client application.    You must include
        an `app_code` with every request."
      operationId: GetrouteJsonGet
      x-api-path-slug: getroute-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: mode
      - in: query
        name: routeid
      responses:
        200:
          description: OK
      tags:
      - Previously
      - Calculated
      - Route
      - Information
  /6.1/flow.json:
    get:
      summary: Flow using Proximity returning Additional Attributes
      description: |-
        *Request traffic flow information using proximity, returning shape and functional class*

        The request is made through combining the `prox` parameter and the `responseattributes` in the request URL. The server also supports an XML response.



        * **prox**  `prox`
         \- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`

        * **responseattributes**  `multi-enum`
         \- A list indicating optional information to be included in the traffic flow data response

         Valid values are : `fc` - functionalClass, `sh` - shape

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: 61FlowJsonGet7
      x-api-path-slug: 6-1flow-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: prox
      - in: query
        name: responseattributes
      responses:
        200:
          description: OK
      tags:
      - Flow
      - Using
      - Proximity
      - Returning
      - Itional
      - Attributes
  /flowtile/newest/normal.day/15/16358/10898/256/png8:
    get:
      summary: Transparent Traffic Map
      description: |-
        *Request a transparent tile with traffic flow information*

        To obtain a transparent map tile displaying traffic flow, use the `flowtile` parameter in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: FlowtileNewestNormalDay151635810898256Png8Get
      x-api-path-slug: flowtilenewestnormal-day151635810898256png8-get
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
      - Traffic
      - Map
  /png32:
    get:
      summary: Transparent Traffic Map via TDA (to be deprecated)
      description: |-
        *Request a transparent tile with traffic flow information*

        Supports custom coloring, functional class filters, DLR rendering, sub-segment traffic rendering.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: Png32Get
      x-api-path-slug: png32-get
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
      - Traffic
      - Map
      - Via
      - TDA
      - (to
      - Be
      - Deprecated)
  /6.0/flowavailability.json:
    get:
      summary: Traffic Flow Availability Data
      description: |-
        *Flow availability requests allow you to see what traffic flow coverage exists in the current Traffic API.*

        T<i></i>he Server also supports an XML response.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: 60FlowavailabilityJsonGet
      x-api-path-slug: 6-0flowavailability-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Traffic
      - Flow
      - Availability
      - Data
  /traffictile/newest/normal.day/15/16358/10898/256/png8:
    get:
      summary: Traffic Map
      description: |-
        *Request a map tile with traffic flow information*

        To obtain a traffic map tile, use the  `traffictile` parameter in the path of the request URL.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: TraffictileNewestNormalDay151635810898256Png8Get
      x-api-path-slug: traffictilenewestnormal-day151635810898256png8-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Traffic
      - Map
  /6.0/incidents.json:
    get:
      summary: Traffic Incidents via Proximity
      description: |-
        *Request traffic incident information within specified area*

        Traffic incidents can be retrieved through several different request types, based on the addressing schemes that they use to specify their geography. Traffic requests can be output to either XML or JSON format. API also supports filters to limit the amount of information provided in the response. Filters are based on on status, criticality, TMC table IDs, profiles, or start and end times, etc.



        * **prox**  `prox`
         \- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`

        * **criticality**  `multi-enum`
         \- A filter that selects incident reports according to criticality,  `0`=critical, `1`=major, `2`=minor,  `3`=lowImpact

         Valid values are : `0` - critical, `1` - major, `2` - minor, `3` - lowImpact

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: 60IncidentsJsonGet3
      x-api-path-slug: 6-0incidents-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: criticality
      - in: query
        name: prox
      responses:
        200:
          description: OK
      tags:
      - Traffic
      - Incidents
      - Via
      - Proximity
  /v1:
    get:
      summary: Venue Clusters within a Bounding Box
      description: |-
        *Request an overview of the number venues across a large area*

        A bounding box is specified using the `bbox` parameter in the request URL.



        * **bbox**  `bbox`
         \- A type of spatial filter. A bounding box specifies the top-right and bottom left corners of an area to search.    e.g. `52.515,13.377;52.134,13.978`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: V1Get3
      x-api-path-slug: v1-get
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
      - Venue
      - Clusters
      - Within
      - Bounding
      - Box
  /1/models-full/DM_12321.js:
    get:
      summary: Full Venue Model
      description: "*Request extended details of places found within a venue*\n\nA
        full model of a venue can be obtained by passing `models-full` in the path
        of the request URL and appending the `id` of the venue in question along with
        associated authentication credentials. \n  \n  Note that the client-side process
        formatting the JSON response may take some time in older browsers.\n\n\n\n*
        **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an `app_id`
        with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an `app_code` with every request.\n\n* **Signature**  `text`\n
        \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n
        \\- Key-Pair-Id"
      operationId: 1ModelsFullDM12321JsGet
      x-api-path-slug: 1modelsfulldm-12321-js-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: Key-Pair-Id
      - in: query
        name: Policy
      - in: query
        name: Signature
      responses:
        200:
          description: OK
      tags:
      - Full
      - Venue
      - Model
  /0/tiles-png/L1/12022001101210030210.png:
    get:
      summary: Venue Map Tile
      description: |-
        *Request an individual venue map tile*

        In addition to the usual `app_id` and `app_code`, three additional parameters are required for authentication purposes. The `Signature`, `Policy` and `Key-Pair-Id` parameters have been obtained from a prior request to the `Signature` endpoint.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Signature**  `text`
         \- Signature

        * **Policy**  `text`
         \- Policy

        * **Key-Pair-Id**  `text`
         \- Key-Pair-Id
      operationId: 0TilesPngL112022001101210030210PngGet
      x-api-path-slug: 0tilespngl112022001101210030210-png-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: Key-Pair-Id
      - in: query
        name: Policy
      - in: query
        name: Signature
      responses:
        200:
          description: OK
      tags:
      - Venue
      - Map
      - Tile
  /0/tiles-ia/L1/12022001101210030210.js:
    get:
      summary: Room Definitions
      description: |-
        *Request a list of the name and shape of rooms found within a single venue map tile*

        Room data associated with a map tile is requested by passing `tiles-ia` in the path of the request URL, along with a known `floor` and `quadkey` and associated authentication credentials.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Signature**  `text`
         \- Signature

        * **Policy**  `text`
         \- Policy

        * **Key-Pair-Id**  `text`
         \- Key-Pair-Id
      operationId: 0TilesIaL112022001101210030210JsGet
      x-api-path-slug: 0tilesial112022001101210030210-js-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: Key-Pair-Id
      - in: query
        name: Policy
      - in: query
        name: Signature
      responses:
        200:
          description: OK
      tags:
      - Room
      - Definitions
  /1/models-poi/DM_7205.js:
    get:
      summary: Places within a Venue
      description: |-
        *Request a list of the places within a venue*

        Details of the individual places to be found within a venue can be obtained by passing `models-poi` in the path of the request URL and appending the `id` of the venue in question along with associated authentication credentials.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Signature**  `text`
         \- Signature

        * **Policy**  `text`
         \- Policy

        * **Key-Pair-Id**  `text`
         \- Key-Pair-Id
      operationId: 1ModelsPoiDM7205JsGet
      x-api-path-slug: 1modelspoidm-7205-js-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: Key-Pair-Id
      - in: query
        name: Policy
      - in: query
        name: Signature
      responses:
        200:
          description: OK
      tags:
      - Places
      - Within
      - Venue
  /0/tiles-ia-b64/L1/12022001101210030210.js:
    get:
      summary: Base64 Encoded Map Tiles
      description: |-
        *Request a base64 encoded map tile and associated room definitions with a single request*

        A base64 encoded map tile together with the room definitions, is requested by passing `tiles-ia-b64` in the path of the request URL, along with a known `floor` and `quadkey` and associated authentication credentials.



        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **Signature**  `text`
         \- Signature

        * **Policy**  `text`
         \- Policy

        * **Key-Pair-Id**  `text`
         \- Key-Pair-Id
      operationId: 0TilesIaB64L112022001101210030210JsGet
      x-api-path-slug: 0tilesiab64l112022001101210030210-js-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: Key-Pair-Id
      - in: query
        name: Policy
      - in: query
        name: Signature
      responses:
        200:
          description: OK
      tags:
      - Base64
      - Encoded
      - Map
      - Tiles
  /findsequence.json:
    get:
      summary: Waypoint Sequence for Hazardous Materials
      description: |-
        *Request an ordered list of destinations for a truck carrying hazardous materials*

        Waypoint sequence calcuations are made using the `findsequence` endpoint and appending  `start` and `end` parameters and consecutively numbered `destination` parameters are used to add intermediate points  to the request. Hazardous material types are added as a comma-delimited list to the  `shippedHazardousGoods` parameter. The list of values is defined in the Enterprise Routing API



        * **start**  `latlng`
         \- Start point for the route calculations.    e.g. `52.515,13.377`

        * **destination1**  `latlng`
         \- A point through which the route must pass.    e.g. `52.6172,13.3833`

        * **destination2**  `latlng`
         \- A point through which the route must pass.    e.g. `52.6172,13.3833`

        * **destination3**  `latlng`
         \- A point through which the route must pass.    e.g. `52.6172,13.3833`

        * **destination4**  `latlng`
         \- A point through which the route must pass.    e.g. `52.6172,13.3833`

        * **end**  `latlng`
         \- End point for the route calculations.    e.g. `50.121,8.925`

        * **improveFor**  `enum`
         \- Whether to improve for time or distance

         Valid values are : `time`, `distance`

        * **mode**  `text`
         \- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled`

        * **shippedHazardousGoods**  `multi-enum`
         \- Truck routing only, list of hazardous materials in the vehicle.

         Valid values are : `combustible`, `corrosive`, `explosive`, `flammable`, `gas`, `harmfulToWater`, `organic`, `other`, `poison`, `poisonousInhalation`, `radioActive`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: FindsequenceJsonGet4
      x-api-path-slug: findsequence-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: destination1
      - in: query
        name: destination2
      - in: query
        name: destination3
      - in: query
        name: destination4
      - in: query
        name: end
      - in: query
        name: improveFor
      - in: query
        name: mode
      - in: query
        name: shippedHazardousGoods
      - in: query
        name: start
      responses:
        200:
          description: OK
      tags:
      - Waypoint
      - SequenceHazardous
      - Materials
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
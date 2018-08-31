---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Map Tile API Filtering Points of Interest
  description: "*Request a map tile including selected points of interest*\n\nPoints
    of interest are displayed by passing the `pois` parameter in the request URL.
    The type of points of interest to be displayed can be filtered by using a hexadecimal
    bitmask.\n  \n\n\n\n* **pois**  `text`\n \\- Displays points of interest if present
    \ \n\n Valid values are : `default`, `alps`, `fleet`, `wings`, `dreamworks`, `flame`,
    `mini`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
    used for the authentication of the client application.    You must include an
    `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_code` with every request."
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
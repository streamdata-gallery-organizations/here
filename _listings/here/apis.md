---
name: HERE
x-slug: here
description: HERE Technologies enables people, enterprises and cities around the world
  to harness the power of location and create innovative solutions that make our lives
  safer and more efficient. We transform information from devices, vehicles, infrastructure
  and...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
x-kinRank: "7"
x-alexaRank: "3011"
tags: HERE
created: "2018-08-30"
modified: "2018-08-30"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/apis.md
specificationVersion: "0.14"
apis:
- name: Batch Geocoder API - Get Job
  x-api-slug: jobspuwwrv32you24y8mnour793chfai36ac-get
  description: "*Request the status of a batch geocoder job*\n\nTo check the status,
    make a request to the `jobs` endpoint  appending the `requestId` and using the
    parameter `action=status `\n  \n\n\n\n* **action**  `enum`\n \\- Type of request
    \ \n\n Valid values are : `cancel`, `runs`, `status`\n\n* **app_code**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_code` with every request.  \n\n*
    **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an `app_id` with
    every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://batch.geocoder.cit.api.here.com//6.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/jobspuwwrv32you24y8mnour793chfai36ac-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/jobspuwwrv32you24y8mnour793chfai36ac-get-openapi.md
- name: Batch Geocoder API - Add Jobs
  x-api-slug: jobs-post
  description: "* Start asynchronously geocoding a large set of addresses in one batch*\n\nSubmit
    an HTTP POST request with `action=run` and attach the input data to the body.
    \n  \n\n\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible behavior
    in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
    used for the authentication of the client application.    You must include an
    `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_code` with every request.\n\n* **action**  `enum`\n
    \\- Type of request\n\n Valid values are : `cancel`, `run`, `status`\n\n* **mailto**
    \ `text`\n \\- Email address where completion notification is sent.\n\n* **header**
    \ `enum`\n \\- If `true`, a header row is included before the results in the output.
    \ \n\n Valid values are : `false`, `true`\n\n* **indelim**  `text`\n \\- \n\n*
    **outdelim**  `text`\n \\- \n\n* **outcols**  `text`\n \\- \n\n* **outputCombined**
    \ `enum`\n \\- \n\n Valid values are : `true`, `false`"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://batch.geocoder.cit.api.here.com//6.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/jobs-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/jobs-post-openapi.md
- name: Custom Location Extension API - Find Locations within a Bounding Box
  x-api-slug: bbox-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://customlocation.cit.api.here.com//v1/search
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/bbox-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/bbox-get-openapi.md
- name: Custom Location Extension API - Filtering by Custom Attributes
  x-api-slug: attribute-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://customlocation.cit.api.here.com//v1/search
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/attribute-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/attribute-get-openapi.md
- name: Custom Location Extension API - Find the Five Nearest Locations
  x-api-slug: proximity-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://customlocation.cit.api.here.com//v1/search
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/proximity-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/proximity-get-openapi.md
- name: Custom Location Extension API - Find Locations along a pre-defined Route
  x-api-slug: routecorridor-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://customlocation.cit.api.here.com//v1/search
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/routecorridor-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/routecorridor-get-openapi.md
- name: Custom Location Extension API - Find Locations using Corridor
  x-api-slug: corridor-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://customlocation.cit.api.here.com//v1/search
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/corridor-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/corridor-get-openapi.md
- name: Geocoder API - Geocode using partial address information
  x-api-slug: geocode-json-get
  description: "*Request the latitude, longitude and details of an address based on
    partial address information*\n\nThis example shows a structured (qualified) geocoding
    request using the `geocode` endpoint. In this structured request the data is provided
    in `country`, `city`, `street` and `housenumber` parameters in the request URL.
    Note that the street name misses the directional (\"W\") and also the street type.
    The omitted directional makes the query ambiguous and the response contains therefore
    two results: One address on West Randolph St and one on East Randolph St.\n  \n\n\n\n*
    **housenumber**  `text`\n \\- The house number or house name\n\n* **street**  `text`\n
    \\- The street name can include suite, apt and floor information.\n\n* **city**
    \ `text`\n \\- City name\n\n* **country**  `text`\n \\- Specify the country or
    list of countries using the country code (3 bytes, ISO 3166-1-alpha-3) or the
    country name\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible
    behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded
    string used for the authentication of the client application.    You must include
    an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://geocoder.cit.api.here.com//6.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/geocode-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/geocode-json-get-openapi.md
- name: Geocoder API - Reverse Geocode Landmarks
  x-api-slug: reversegeocode-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://geocoder.cit.api.here.com//6.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/reversegeocode-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/reversegeocode-json-get-openapi.md
- name: Geocoder API - Multi-reverse Geocode Addresses
  x-api-slug: multireversegeocode-json-post
  description: "*Request the addresses of up to one hundred locations with one multi-reverse
    geocoding request*\n\nThe body of the HTTP POST request contains the coordinates
    and optional radius in the `prox` parameter and an optional numeric identifier
    in the `id` parameter as plain text, one line per pair of coordinates. The identifier
    associates each result with the corresponding input. If no id is provided the
    system creates one starting with 0.\n  \n\n\n\n* **mode**  `enum`\n \\- Search
    for prominent landmarks nearby  \n\n Valid values are : `retrieveAddresses`, `retrieveAreas`,
    `retrieveLandmarks`, `retrieveAll`, `trackPosition`\n\n* **gen**  `number`\n \\-
    Enables/disables backward incompatible behavior in the API\n\n* **app_id**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_id` with every request.\n\n* **app_code**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_code` with every request.\n\n*
    **Content-Type**  `header`\n\n  Accept any content in return\n\n* **Cache-Control**
    \ `header`\n\n  Ensure that the request is always passed to server so that latest
    response is retrieved"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://geocoder.cit.api.here.com//6.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/multireversegeocode-json-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/multireversegeocode-json-post-openapi.md
- name: Map Image API - Map Image using Bounding Box
  x-api-slug: mapview-get
  description: |-
    *Request an image of a map based around a given area*

    To specify a bounding box, add the `bbox` parameter to the request URL. On desktop browsers, redirection to `here.com` will occur automatically unless the `nord` parameter is also added to URL.



    * **bbox**  `text`
     \- Bounding box of the map specifying the top-right and bottom left corners.    e.g. `52.515,13.377,52.134,13.978`

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://image.maps.cit.api.here.com//mia/1.6
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/mapview-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/mapview-get-openapi.md
- name: Map Image API - Map Image with Polylines
  x-api-slug: route-get
  description: "*Request an image of a map including a polyline*\n\nIt supports also
    different map schemes, image sizes; image formats as \r\nwell as zooming out from
    automatically calculated zoom level.\n  \n\n\n\n* **r0**  `text`\n \\- List of
    coordinates describing the first route\n\n* **r1**  `text`\n \\- List of coordinates
    describing the second route\n\n* **m0**  `text`\n \\- First route marker on the
    map\n\n* **m1**  `text`\n \\- Second route marker on the map\n\n* **lc0**  `text`\n
    \\- Color of the first route line displayed on the map\n\n* **sc0**  `text`\n
    \\- Shadow color of the first route line displayed on the map\n\n* **lw0**  `number`\n
    \\- Width of the first route line displayed on the map\n\n* **lc1**  `text`\n
    \\- Color of the second route line displayed on the map\n\n* **sc1**  `text`\n
    \\- Shadow color of the second route line displayed on the map\n\n* **lw1**  `number`\n
    \\- Width of the second route line displayed on the map\n\n* **w**  `number`\n
    \\- Image width in pixels, maximum 2048.\n\n* **app_id**  `text`\n \\- A 20 byte
    Base64 URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://image.maps.cit.api.here.com//mia/1.6
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/route-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/route-get-openapi.md
- name: Map Tile API - Terrain Map
  x-api-slug: terrain-day76645256png8-get
  description: |-
    *Request a terrain map tile*

    Terrain map tile are available by passing `terrain.day` in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/terrain-day76645256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/terrain-day76645256png8-get-openapi.md
- name: Map Tile API - Multiple Base64 Encoded Map Tiles
  x-api-slug: maptilenewestnormal-day63024256png8-get
  description: "*Request multiple base64 encoded map tiles*\n\nA square consisting
    of multiple base64 encoded tiles is requested by adding the parameters `output=base64`
    and `range=NxN` to the request URL. The `column` and `row` in the path of the
    URL, defining the top left-hand corner of the tile group must be divisible by
    the value of the `range` parameter.\n  \n  Click on the response to decode the
    tiles returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return
    the tile as base64 encoded text.\n\n* **range**  `enum`\n \\- Indicates the size
    of the array of tiles returned. Valid values are `2x2`, `3x3` or `4x4`\n\n Valid
    values are : `2x2`, `3x3`, `4x4`\n\n* **app_id**  `text`\n \\- A 20 byte Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day63024256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day63024256png8-get-openapi.md
- name: Map Tile API - Color-reduced Transit Map
  x-api-slug: maptilenewestnormal-day-transit1220741409256png8-get
  description: |-
    *Request a color-reduced map tile with public transport*

    Color-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day-transit1220741409256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day-transit1220741409256png8-get-openapi.md
- name: Map Tile API - Filtering Points of Interest
  x-api-slug: maptilenewestnormal-day161874325072256png8-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day161874325072256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day161874325072256png8-get-openapi.md
- name: Map Tile API - Hybrid Map
  x-api-slug: hybrid-day485256png8-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/hybrid-day485256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/hybrid-day485256png8-get-openapi.md
- name: Map Tile API - Truck Restrictions Map
  x-api-slug: trucktilenewestnormal-day1221991342256png8-get
  description: |-
    *Request a street map tile showing restrictions for heavy vehicles*

    To obtain a map tile displaying route restrictions for trucks, use the `trucktile` parameter in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/trucktilenewestnormal-day1221991342256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/trucktilenewestnormal-day1221991342256png8-get-openapi.md
- name: Map Tile API - Toll Zone Map
  x-api-slug: maptilenewestnormal-day9255170256png8-get
  description: |-
    *Request a street map tile highlighting congestion and environmental toll zones*

    To highlight such toll zones, add the `congestion` parameter to the request URL.



    * **congestion**  `null`
     \- Flag to indicate if congestion zones are to be shown on the map.

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day9255170256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day9255170256png8-get-openapi.md
- name: Map Tile API - Point of Interest Categories
  x-api-slug: metapois-get
  description: "*Request point of interest category information*\n\nTo make a request
    for point-of-interest information, use `meta/pois` in the path of the request
    URL.\n  \n\n\n\n* **output**  `enum`\n \\- A 20 byte Base64 URL-safe encoded string
    used for the authentication of the client application.    You must include an
    `app_id` with every request.\n\n Valid values are : `json`, `text`\n\n* **app_id**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_id` with every request..
    \ \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used
    for the authentication of the client application.    You must include an `app_code`
    with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metapois-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metapois-get-openapi.md
- name: Map Tile API - Copyright Information
  x-api-slug: copyrightnewest-get
  description: "*Request map tile copyright information*\n\nTo make a request for
    copyright information, use the `copyright` parameter in the path of the request
    URL.\n  \n  Note that the client-side process formatting the JSON response may
    take some time in older browsers.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte
    Base64 URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/copyrightnewest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/copyrightnewest-get-openapi.md
- name: Map Tile API - Satellite Map
  x-api-slug: satellite-day51512256png8-get
  description: |-
    *Request a satellite map tile*

    Satellite map tiles do not display labels and are available by passing `satellite.day` in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/satellite-day51512256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/satellite-day51512256png8-get-openapi.md
- name: Map Tile API - Foreign Language Support
  x-api-slug: maptilenewestnormal-day111196595256png8-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day111196595256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day111196595256png8-get-openapi.md
- name: Map Tile API - Fleet Vehicle Map
  x-api-slug: maptilenewestnormal-day1340932723256png8-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day1340932723256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day1340932723256png8-get-openapi.md
- name: Map Tile API - Support for Multiple Languages
  x-api-slug: maptilenewestnormal-day1366933575256png8-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day1366933575256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day1366933575256png8-get-openapi.md
- name: Map Tile API - Base64 Encoded Map Tile
  x-api-slug: maptilenewestnormal-day11525761256png8-get
  description: "*Request a base64 encoded map tile*\n\nBase64 encoded tiles are requested
    by adding the parameter `output=base64` to the request URL.\n  \n  Click on the
    response to decode the tile returned.\n\n\n\n* **output**  `text`\n \\- Indicates
    whether to return the tile as base64 encoded text.\n\n* **app_id**  `text`\n \\-
    A 20 byte Base64 URL-safe encoded string used for the authentication of the client
    application.    You must include an `app_id` with every request.\n\n* **app_code**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day11525761256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day11525761256png8-get-openapi.md
- name: Map Tile API - Color-reduced Street Map
  x-api-slug: maptilenewestnormal-day-grey11525761256png8-get
  description: |-
    *Request a greyed out street map tile*

    Maps using a reduced color palette can be requested by passing `normal.day.grey` in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day-grey11525761256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/maptilenewestnormal-day-grey11525761256png8-get-openapi.md
- name: Map Tile API - Map Tile Type Information
  x-api-slug: info-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/info-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/info-get-openapi.md
- name: Map Tile API - Transparent Truck Restrictions Map
  x-api-slug: truckonlytilenewestnormal-day1221991342256png8-get
  description: |-
    *Request a transparent tile showing restrictions for heavy vehicles only*

    To obtain a transparent map tile displaying route restrictions for trucks, use the `truckonlytile` parameter in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/truckonlytilenewestnormal-day1221991342256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/truckonlytilenewestnormal-day1221991342256png8-get-openapi.md
- name: Places API - Search Suggestions
  x-api-slug: suggest-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://places.demo.api.here.com//places/v1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/suggest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/suggest-get-openapi.md
- name: Places API - Place Categories
  x-api-slug: categoriesplaces-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://places.demo.api.here.com//places/v1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/categoriesplaces-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/categoriesplaces-get-openapi.md
- name: Places API - Explore Popular Places
  x-api-slug: discoverexplore-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://places.demo.api.here.com//places/v1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/discoverexplore-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/discoverexplore-get-openapi.md
- name: Places API - Explore Nearby Places
  x-api-slug: discoverhere-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://places.demo.api.here.com//places/v1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/discoverhere-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/discoverhere-get-openapi.md
- name: Places API - One-Box Search
  x-api-slug: discoversearch-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://places.demo.api.here.com//places/v1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/discoversearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/discoversearch-get-openapi.md
- name: Public Transport API - Find Stations by Name
  x-api-slug: searchby-name-json-get
  description: "*Request a list of public transit stations based on name*\n\nA station
    search request can be made using the `search/by_name.json` endpoint and adding
    the `name` parameter. The focal point of the search is defined using the `x` and
    `y` parameters. The number of results can be further restricted by `max `and the
    `radius `parameters.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center
    point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude
    of the center point of your search.    e.g. `52.515`\n\n* **name**  `text`\n \\-
    Specifies the name or a part of the name of the station to search for and can
    be one word, multiple words or partial word separated by either comma or space.\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request.\n\n* **max**
    \ `number`\n \\- Specifies the maximum number of stations/stops included in the
    response.\n  The minimum value is 1 and the maximum value is not limited.\n  The
    default value is 5.     \n\n* **method**  `enum`\n \\- Specifies if the matching
    method is *fuzzy* or *strict*.\n  The default value is *fuzzy*.\n    * fuzzy -
    search for stations with the name having similar sounding and/or similar spelling
    to the names requested\n    * strict - search for stations with the name exactly
    matching the names requested or contains it as its part.\n\n   Valid values are
    : `fuzzy`, `strict`\n\n* **radius**  `number`\n \\- Specifies a radius in meters
    when combined with a center point defines the area of the search. The minimum
    value is 0 and the maximum value is not limited.\n  The default value is 20000km."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/searchby-name-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/searchby-name-json-get-openapi.md
- name: Public Transport API - Avoid Transit Routes Involving Transfers
  x-api-slug: metarouterrestrouteservicev2route-json-get
  description: "*Request a direct public transit route excluding changes and transfers*\n\nPublic
    transit routes can be requested using the `metarouter/rest/routeservice/v2/route.json`
    endpoint. The `changes `parameter is used to indicate the number of changes or
    transfers desired. \n\n\n\n* **startX**  `number`\n \\- The longitude of the start
    point of your journey.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude
    of the start point of your journey.    e.g. `52.515`\n\n* **destX**  `number`\n
    \\- The longitude of the destination point of your journey.    e.g. `13.377`\n\n*
    **destY**  `number`\n \\- The latitude of the destination point of your journey.
    \   e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request.\n\n* **routing**
    \ `enum`\n \\- Type of routing response required.  tt: time-table routing, i.e.
    route response will show scheduled arrival/departure times of the transit at the
    stations.  sr: simple (or estimated) routing, i.e. route response will only show
    \nthe transit journey but without scheduled arrival/departure times.  all: for
    both estimated and time-table routing.  Default: tt  \n\n    Valid values are
    : `tt`, `sr`, `all`\n\n* **changes**  `enum`\n \\- Maximum number of changes or
    transfers. \n                Valid values: 0-6 or -1. Default: -1 (any number
    of transfers permitted).\n\n    >**NOTE:** In areas where this parameter is not
    supported the route response will show an attribute `sup_changes=0` in the `Connections`
    node.\n\n    Valid values are : `-1`, `0`, `1`, `2`, `3`, `4`, `5`, `6`"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestrouteservicev2route-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestrouteservicev2route-json-get-openapi.md
- name: Public Transport API - Reachability of an Area Within a Specific Time
  x-api-slug: isochronev1search-json-get
  description: "*Request a list of the public transit stations that can be reached
    in a given time*\n\nTo find the stations reachable in a specified time use the
    `isochrone/v1/search.json` endpoint specifying a center point using the `x` and
    `y` parameters and a maximum total duration in minutes using the `max_dur `parameter.\n
    \ \n\n\n\n* **max_dur**  `number`\n \\- Maximum duration of the journeys, in minutes.
    \  Minimum = 5, Maximum = 90.    The default duration is 15 minutes.    \n\n*
    **y**  `number`\n \\- The latitude of the start point of your journey.    e.g.
    `52.515`  \n\n* **x**  `number`\n \\- The longitude of the start point of your
    journey.    e.g. `13.377`    \n\n* **time**  `text`\n \\- Specifies the time in
    ISO 8601 (for example, 2015-10-18T06:36:40)\n        format. \n\n* **app_id**
    \ `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an app_code and app_code with every
    request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string
    used for the authentication of the client application.    You must include an
    app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/isochronev1search-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/isochronev1search-json-get-openapi.md
- name: Public Transport API - All Next Departures (deprecated)
  x-api-slug: metarouterrestboardservicev1multiboard-json-get
  description: "*Request a list of all next departure times and destinations from
    a location.*\n\nAll next departures information can be requested using the `metarouter/rest/boardservice/v1/multiboard.json`
    and specifying a `time` and `coordinates. `The maximum numbers of nearby stations
    and number of departures per station can be restricted by using the `max_stn`
    and `max` parameters, respectively.\n  \n  <b>NOTE:</b> This API has been deprecated
    and replaced with 2 new endpoints. Please see \n  <b><i>All Next Departures from
    a Location </i></b>and <b><i>All Next Departures for a list of Stations </i></b>for
    more details.\n  \n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n*
    **startX**  `number`\n \\- The longitude of the center point of your search.    e.g.
    `13.377`\n\n* **startY**  `number`\n \\- The latitude of the center point of your
    search.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request.\n\n* **max**
    \ `text`\n \\- The  maximum number of next departures per station to be included
    in the response.    The default value is 40.  \n\n* **max_stn**  `text`\n \\-
    \ The maximum number of stations for which departures are required. The default
    value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit binary number, where each
    bit represents one type of transit.  \n  0: High-speed Trains  \n  1: Intercity/EuroCity
    Trains  \n  2: Inter-regional and fast trains  \n  3: Regional and other trains
    \ \n  4: City trains  \n  5: Buses  \n  6: Boat/Ferries  \n  7: Metro/Subway  \n
    \ 8: Tram  \n  9: Ordered services/Taxi  \n  10: Inclined/Funicular  \n  11: Aerial/Cable
    Car  \n  12: Rapid Bus  \n  13: Monorail  \n  14: Air plane  \n  15: Not yet defined
    \ \n  The default is 1111111111111111, meaning all supported transit types are
    permitted."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev1multiboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev1multiboard-json-get-openapi.md
- name: Public Transport API - Transit Coverage Nearby
  x-api-slug: coveragev1nearby-json-get
  description: "*Request a list of transit operators and station coverage nearby*\n\nOperator
    coverage is requested using the `coverage/v1/nearby.json` endpoint specifying
    the location using the `x` and `y` parameters.\n\n\n\n* **details**  `enum`\n
    \\- Don't show line info in Explored Coverage\n\n    Valid values are : `0` -
    disabled, `1` - enabled\n\n* **y**  `number`\n \\- The latitude of the center
    point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude
    of the center point of your search.    e.g. `13.377`\n\n* **chinaconfig**  `enum`\n
    \\- A switch that allows grouping results from Taiwan\ntogether with results from
    China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid
    values are : `0` - disabled, `1` - enabled\n\n* **app_id**  `text`\n \\- A 20
    bytes Base64 URL-safe encoded string used for the authentication of the client
    application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/coveragev1nearby-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/coveragev1nearby-json-get-openapi.md
- name: Public Transport API - Transit Coverage Within a City
  x-api-slug: coveragev1search-json-get
  description: "*Request a list of transit operator coverage within a specified city*\n\nA
    list of operators working within a city is requested using the `coverage/v1/search.json`
    endpoint. The city is specified using the  `q` parameter.\n\n\n\n* **q**  `text`\n
    \\- The name or a part of the name of the city to search.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request.\n\n* **max**  `number`\n \\- Maximum number of
    results to be returned. Default is null.\n\n* **details**  `enum`\n \\- With this
    value set to 1, the list of supported operators and population of the city is
    returned.   When the value is set to 0, only the list of matching city names will
    be returned.  Default value = 1\n\n    Valid values are : `0` - disabled, `1`
    - enabled\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results
    from Taiwan\ntogether with results from China.      \n\n    Valid values are :
    `0` - disabled, `1` - enabled\n\n* **lang**  `text`\n \\- The language of the
    response. The value complies with the ISO 639-1 standard and defaults to <i>en</i>."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/coveragev1search-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/coveragev1search-json-get-openapi.md
- name: Public Transport API - Find Stations by ID
  x-api-slug: searchby-stopids-json-get
  description: "*Request details of a specific transit station based on a previous
    request*\n\nStation details are requested using the `search/by_stopids.json` endpoint
    and appending a comma delimited list of `stop-ids` to the request URL. Usually,
    the request to this endpoint will be called after making a station search request,
    to obtain a list of stations Ids.\n  \n\n\n\n* **stopIds**  `text`\n \\- Specifies
    a list of stopIds separated by comma. Each stopId must contain at least 6 characters
    and must not exceed a maximum of 1000 characters.     The format of a station
    Id is 123456789#100. Only the first 9-digits are mandatory and if the full Id
    is to be used, the `#` character must be encoded as `%23`.      \n\n* **lang**
    \ `text`\n \\- A language of the response. \n\n* **app_id**  `text`\n \\- A 20
    bytes Base64 URL-safe encoded string used for the authentication of the client
    application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/searchby-stopids-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/searchby-stopids-json-get-openapi.md
- name: Public Transport API - Find Stations Nearby
  x-api-slug: searchby-geocoord-json-get
  description: "*Request a list of public transit stations within a given geo-location.*\n\nTo
    find the nearest stations use the `search/by_geocoord.json` endpoint specifying
    a center point using the `x` and `y` parameters and a search radius in meters
    using the `radius` parameter. `Max` value can also be used to restrict the number
    of results shown in the response.\n\n\n\n* **y**  `number`\n \\- The latitude
    of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\-
    The longitude of the center point of your search.    e.g. `13.377`\n\n* **radius**
    \ `number`\n \\- Specifies a radius in meters when combined with the geo-coordinates
    defines the area of the search. The default value is 500m.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the maximum
    number of stations/stops included in the response. \n          The default value
    is 5. The minimum value is 1 and the maximum value is not limited."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/searchby-geocoord-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/searchby-geocoord-json-get-openapi.md
- name: Public Transport API - Find Transit Coverage in Cities Nearby
  x-api-slug: coveragev1city-json-get
  description: "*Request a list of transit operators available in cities nearby*\n\nCity
    coverage can be found using the `coverage/v1/city.json` endpoint. The `x` and
    `y` parameters specify the location of the search.\n  The response also includes
    the number of transit lines and transit stops available for each city.\n  \n\n\n\n*
    **x**  `number`\n \\- The longitude of the center point of your search.    e.g.
    `13.377`\n\n* **y**  `number`\n \\- The latitude of the center point of your search.
    \   e.g. `52.515`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping
    results from Taiwan\ntogether with results from China.    When enabled, Taiwan
    will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1`
    - enabled\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined
    with a center point defines the area of the search.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/coveragev1city-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/coveragev1city-json-get-openapi.md
- name: Public Transport API - Next Nearby Departures from a Station
  x-api-slug: metarouterrestboardservicev2stationboard-json-get
  description: "*Request a list of next departure times and destinations of a particular
    station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
    and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained
    from making a prior call to one of the station search (by name or by geo-coordinates)
    endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**
    \ `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only
    the first 9-digits are mandatory and if the full Id is to be used, the `#` character
    must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **strict**  `enum`\n \\- When `strict=1` the board will include only departures
    from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-openapi.md
- name: Public Transport API - All Next Departures for a list of Stations
  x-api-slug: metarouterrestboardservicev1multiboardby-stopids-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev1multiboardby-stopids-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev1multiboardby-stopids-json-get-openapi.md
- name: Public Transport API - All Next Departures from a Location
  x-api-slug: metarouterrestboardservicev1multiboardby-geocoord-json-get
  description: "*Request a list of all next departure times and destinations from
    a given location.*\n\nAll next departures from a given location can be requested
    using the `metarouter/rest/boardservice/v1/multiboard/by_geocoord.json` and specifying
    a `time` and `coordinates. `The maximum numbers of nearby stations and number
    of departures per station can be restricted by using the `max_stn` and `max` parameters,
    respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n*
    **startX**  `number`\n \\- The longitude of the center point of your search.    e.g.
    `13.377`\n\n* **startY**  `number`\n \\- The latitude of the center point of your
    search.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request.\n\n* **max**
    \ `text`\n \\- The  maximum number of next departures per station to be included
    in the response.     The default value is 40.  \n\n* **max_stn**  `text`\n \\-
    \ The maximum number of stations for which departures are required.     The default
    value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit binary number, where each
    bit represents one type of transit.  \n  0: High-speed Trains  \n  1: Intercity/EuroCity
    Trains  \n  2: Inter-regional and fast trains  \n  3: Regional and other trains
    \ \n  4: City trains  \n  5: Buses  \n  6: Boat/Ferries  \n  7: Metro/Subway  \n
    \ 8: Tram  \n  9: Ordered services/Taxi  \n  10: Inclined/Funicular  \n  11: Aerial/Cable
    Car  \n  12: Rapid Bus  \n  13: Monorail  \n  14: Air plane  \n  15: Not yet defined
    \ \n  The default is 1111111111111111, meaning all supported transit types are
    permitted."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev1multiboardby-geocoord-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/metarouterrestboardservicev1multiboardby-geocoord-json-get-openapi.md
- name: Platform Data Extension API - Platform Static Data
  x-api-slug: static-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://pde.cit.api.here.com//1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/static-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/static-json-get-openapi.md
- name: Platform Data Extension API - Available Map Data Layers
  x-api-slug: doclayers-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://pde.cit.api.here.com//1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/doclayers-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/doclayers-json-get-openapi.md
- name: Platform Data Extension API - Platform Data
  x-api-slug: tile-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://pde.cit.api.here.com//1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/tile-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/tile-json-get-openapi.md
- name: Platform Data Extension API - Available Attributes
  x-api-slug: docattributes-json-get
  description: "*Request which map data layers contain which attributes*\n\nTo make
    a request for map data layer information, use the `attributes``.json` endpoint,
    supplying the `release` and `region` parameters.\n  \n\n\n\n* **region**  `text`\n
    \\- Map Coverage Region.    e.g. `APAC`, `NA`, `EU`\n\n* **release**  `text`\n
    \\- Map release quarter    e.g. `2014Q4` or `LATEST`\n\n* **app_id**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_id` with every request.\n\n* **app_code**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://pde.cit.api.here.com//1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/docattributes-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/docattributes-json-get-openapi.md
- name: Platform Data Extension API - Map Data Availability and Freshness
  x-api-slug: docmaps-json-get
  description: |-
    *Request the release date and area covered by each available map region*

    To make a request for release date information, use the `maps.json` endpoint.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://pde.cit.api.here.com//1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/docmaps-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/docmaps-json-get-openapi.md
- name: Platform Data Extension API - Available Attributes within a Map Data Layer
  x-api-slug: doclayer-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://pde.cit.api.here.com//1
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/doclayer-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/doclayer-json-get-openapi.md
- name: Routing API - Avoid motorways
  x-api-slug: calculateroute-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://route.cit.api.here.com//routing/7.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/calculateroute-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/calculateroute-json-get-openapi.md
- name: Routing API - Many to many matrix routing
  x-api-slug: calculatematrix-json-get
  description: "*Matrix routing request with three start points and five destinations*\n\nMatrix
    calculations are made using the `calculatematrix` endpoint and appending a three
    start parameters (`start0, ``start1, ``start2)` and multiple consecutively numbered
    `destination` parameters to the request.\n  \n\n\n\n* **start0**  `latlng`\n \\-
    First start point for the route calculations.    e.g. `52.515,13.377`  \n\n* **start1**
    \ `latlng`\n \\- Second start point for the route calculations.    e.g. `52.515,13.377`
    \ \n\n* **start2**  `latlng`\n \\- Third start point for the route calculations.
    \   e.g. `52.515,13.377`  \n\n* **destination0**  `latlng`\n \\- First destination
    point for the route calculations.    e.g. `52.4,13.5`  \n\n* **destination1**
    \ `latlng`\n \\- Second destination point for the route calculations.    e.g.
    `52.4,13.5`  \n\n* **destination2**  `latlng`\n \\- Third destination point for
    the route calculations.    e.g. `52.4,13.5`  \n\n* **destination3**  `latlng`\n
    \\- Fourth destination point for the route calculations.    e.g. `52.4,13.5`    \n\n*
    **destination4**  `latlng`\n \\- Fifth destination point for the route calculations.
    \   e.g. `52.4,13.5`  \n\n* **mode**  `text`\n \\- Routing mode determines how
    the route is calculated.    e.g. `fastest;car;traffic:disabled.`  \n\n* **app_id**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an app_id with every request.    \n\n*
    **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code with
    every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://route.cit.api.here.com//routing/7.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/calculatematrix-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/calculatematrix-json-get-openapi.md
- name: Routing API - Time-based isoline with destination as center
  x-api-slug: calculateisoline-json-get
  description: "*Request an isoline that will reach a destination within a given time*\n\nTime-based
    reverse flow requests are made using the `calculateisoline` endpoint and specifying
    the `destination` and `rangetype=time` parameters.\n\n\n\n* **mode**  `text`\n
    \\- Routing mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`\n\n*
    **destination**  `latlng`\n \\- Destination of the reverse flow calculation.    e.g.
    `52.515,13.377`\n\n* **rangetype**  `text`\n \\- Specifies type of range. Possible
    values are distance, time. For distance the unit is  meters. For time the unit
    is seconds.  rangetype=distance  rangetype=time    \n\n* **range**  `number`\n
    \\- Range of isoline. Several comma separated values can be specified. The unit
    is defined by  parameter rangetype  range=1000  range=1000,2000,3000  \n\n* **app_id**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_id` with every request.
    \ \n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used
    for the authentication of the client application.    You must include an `app_code`
    with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://route.cit.api.here.com//routing/7.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/calculateisoline-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/calculateisoline-json-get-openapi.md
- name: Routing API - Link Information using linkId
  x-api-slug: getlinkinfo-json-get
  description: "*Request detailed information about a path segment in the routing
    network given a linkid*\n\nLink information can be retrieved using the `getlinkinfo`
    endpoint, by specifying one or more comma separated linkIds using the `linkids`
    parameter. The `linkids` have been generated from a previous request. Note that
    positive direction '+' in link Ids has to be URL encoded.\n  \n  \n\n\n\n* **linkids**
    \ `text`\n \\- Link identifiers for which the detailed information is being requested.\n\n*
    **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an `app_id` with
    every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded
    string used for the authentication of the client application.    You must include
    an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://route.cit.api.here.com//routing/7.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/getlinkinfo-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/getlinkinfo-json-get-openapi.md
- name: Routing API - Previously calculated route information
  x-api-slug: getroute-json-get
  description: "*Request information about a previously calculated route*\n\nPrevious
    routes can be retrieved using the `getroute` endpoint and appending a `routeid`
    to the request. The `routeid` in question has been generated from a previous request.
    Note that server map updates usually invalidates `routeid` value computed on previous
    map versions. If it is the case, the `routeid` computation should be requested
    again on the map in current  use.\n  \n\n\n\n* **mode**  `text`\n \\- Routing
    mode determines how the route is calculated.    e.g. `fastest;car;traffic:disabled.`
    \ \n\n* **routeid**  `text`\n \\- Route identifier for which the detailed route
    information is being requested.  \n\n* **app_id**  `text`\n \\- A 20 byte Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_id` with every request.  \n\n* **app_code**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://route.cit.api.here.com//routing/7.2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/getroute-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/getroute-json-get-openapi.md
- name: Traffic API - Flow using Proximity returning Additional Attributes
  x-api-slug: 6-1flow-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://tiles.traffic.cit.api.here.com//traffic/6.0/tiles/8/133/86/256
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/6-1flow-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/6-1flow-json-get-openapi.md
- name: Traffic API - Transparent Traffic Map
  x-api-slug: flowtilenewestnormal-day151635810898256png8-get
  description: |-
    *Request a transparent tile with traffic flow information*

    To obtain a transparent map tile displaying traffic flow, use the `flowtile` parameter in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://tiles.traffic.cit.api.here.com//traffic/6.0/tiles/8/133/86/256
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/flowtilenewestnormal-day151635810898256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/flowtilenewestnormal-day151635810898256png8-get-openapi.md
- name: Traffic API - Transparent Traffic Map via TDA (to be deprecated)
  x-api-slug: png32-get
  description: |-
    *Request a transparent tile with traffic flow information*

    Supports custom coloring, functional class filters, DLR rendering, sub-segment traffic rendering.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://tiles.traffic.cit.api.here.com//traffic/6.0/tiles/8/133/86/256
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/png32-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/png32-get-openapi.md
- name: Traffic API - Traffic Flow Availability Data
  x-api-slug: 6-0flowavailability-json-get
  description: |-
    *Flow availability requests allow you to see what traffic flow coverage exists in the current Traffic API.*

    T<i></i>he Server also supports an XML response.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://tiles.traffic.cit.api.here.com//traffic/6.0/tiles/8/133/86/256
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/6-0flowavailability-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/6-0flowavailability-json-get-openapi.md
- name: Traffic API - Traffic Map
  x-api-slug: traffictilenewestnormal-day151635810898256png8-get
  description: |-
    *Request a map tile with traffic flow information*

    To obtain a traffic map tile, use the  `traffictile` parameter in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://tiles.traffic.cit.api.here.com//traffic/6.0/tiles/8/133/86/256
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/traffictilenewestnormal-day151635810898256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/traffictilenewestnormal-day151635810898256png8-get-openapi.md
- name: Traffic API - Traffic Incidents via Proximity
  x-api-slug: 6-0incidents-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://tiles.traffic.cit.api.here.com//traffic/6.0/tiles/8/133/86/256
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/6-0incidents-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/6-0incidents-json-get-openapi.md
- name: Venue Maps - Venue Clusters within a Bounding Box
  x-api-slug: v1-get
  description: |-
    *Request an overview of the number venues across a large area*

    A bounding box is specified using the `bbox` parameter in the request URL.



    * **bbox**  `bbox`
     \- A type of spatial filter. A bounding box specifies the top-right and bottom left corners of an area to search.    e.g. `52.515,13.377;52.134,13.978`

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://signature.venue.maps.cit.api.here.com//venues/signature
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/v1-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/v1-get-openapi.md
- name: Venue Maps - Full Venue Model
  x-api-slug: 1modelsfulldm-12321-js-get
  description: "*Request extended details of places found within a venue*\n\nA full
    model of a venue can be obtained by passing `models-full` in the path of the request
    URL and appending the `id` of the venue in question along with associated authentication
    credentials. \n  \n  Note that the client-side process formatting the JSON response
    may take some time in older browsers.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte
    Base64 URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_code` with every request.\n\n*
    **Signature**  `text`\n \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n*
    **Key-Pair-Id**  `text`\n \\- Key-Pair-Id"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://signature.venue.maps.cit.api.here.com//venues/signature
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/1modelsfulldm-12321-js-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/1modelsfulldm-12321-js-get-openapi.md
- name: Venue Maps - Venue Map Tile
  x-api-slug: 0tilespngl112022001101210030210-png-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://signature.venue.maps.cit.api.here.com//venues/signature
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/0tilespngl112022001101210030210-png-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/0tilespngl112022001101210030210-png-get-openapi.md
- name: Venue Maps - Room Definitions
  x-api-slug: 0tilesial112022001101210030210-js-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://signature.venue.maps.cit.api.here.com//venues/signature
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/0tilesial112022001101210030210-js-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/0tilesial112022001101210030210-js-get-openapi.md
- name: Venue Maps - Places within a Venue
  x-api-slug: 1modelspoidm-7205-js-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://signature.venue.maps.cit.api.here.com//venues/signature
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/1modelspoidm-7205-js-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/1modelspoidm-7205-js-get-openapi.md
- name: Venue Maps - Base64 Encoded Map Tiles
  x-api-slug: 0tilesiab64l112022001101210030210-js-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://signature.venue.maps.cit.api.here.com//venues/signature
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/0tilesiab64l112022001101210030210-js-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/0tilesiab64l112022001101210030210-js-get-openapi.md
- name: Waypoint Sequence Extension API - Waypoint Sequence for Hazardous Materials
  x-api-slug: findsequence-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://wse.cit.api.here.com//2
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/findsequence-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/findsequence-json-get-openapi.md
- name: Weather API - Multi-Language Support
  x-api-slug: report-json-get
  description: |-
    *Request current weather conditions in a foreign language*

    The language of the weather report is altered by adding the `language` parameter to the request URL.



    * **product**  `enum`
     \- The type of information to request

     Valid values are : `observation`, `forecast_7days`, `forecast_7days_simple`, `forecast_hourly`, `forecast_astronomy`, `alerts`, `nws_alerts`

    * **latitude**  `number`
     \- Latitude of the weather forecast.    e.g. `52.5159`

    * **longitude**  `number`
     \- Longitude of the weather forecast.    e.g. `13.3777`

    * **oneobservation**  `enum`
     \- A flag to indicate only one observation is required.

     Valid values are : `true`, `false`

    * **language**  `enum`
     \- The language for the observations within the forecast.

     Valid values are : `af-ZA` - Afrikaans, `sq` - Albanian, `am-ET` - Amharic, `ar` - Arabic, `as-IN` - Assamese, `az-AZ` - Azerbaijani, `eu` - Basque, `be` - Belarusian, `bn-BD` - Bengali-bd, `bn` - Bengali, `bs-BA` - Bosnian, `bg-BG` - Bulgarian, `ca` - Catalan, `zh-CN` - Chinese (PRC), `zh-HK` - Chinese (HK), `zh-TW` - Chinese (TW), `hr-HR` - Croatian, `cs-CZ` - Czech, `da-DK` - Danish, `nl-NL` - Dutch, `en` - English, `en-US` - English (US), `et-EE` - Estonian, `fa` - Farsi, `fa-AF` - Farsi-af, `fi-FI` - Finnish, `fr-CA` - French (CA), `fr` - French, `gl` - Galician, `ka-GE` - Georgian, `de` - German, `el-GR` - Greek, `gu-IN` - Gujarati, `ha` - Hausa, `he-IL` - Hebrew, `hi-IN` - Hindi, `hu-HU` - Hungarian, `is-IS` - Icelandic, `ig-NG` - Igbo, `id-ID` - Indonesian, `it` - Italian, `ja-JP` - Japanese, `kn-IN` - Kannada, `ks-IN` - Kashmiri, `kk-KZ` - Kazakh, `km-KH` - Khmer, `ky-KG` - Kirghiz, `ko-KR` - Korean, `lo-LA` - Lao, `lv-LV` - Latvian, `ln` - Lingala, `lt-LT` - Lithuanian, `mk-MK` - Macedonian, `mg-MG` - Malagasy, `ms-MY` - Malay, `ml-IN` - Malayalam, `mr-IN` - Marathi, `mn-MN` - Mongolian, `no-NO` - Norwegian, `or-IN` - Oriya, `pl-PL` - Polish, `pt-BR` - Portuguese (BR), `pt-PT` - Portuguese (PT), `pa` - Punjabi, `ps` - Pushto, `ro-RO` - Romanian, `ru-RU` - Russian, `sr-YU` - Serbian, `st` - Sesotho, `si-LK` - Sinhala, `sk-SK` - Slovak, `sl-SL` - Slovene, `es-ES` - Spanish, `es-US` - Spanish (US), `sw` - Swahili, `sv` - Swedish, `tl-PH` - Tagalog, `ta` - Tamil, `te-IN` - Telugu, `th-TH` - Thai, `tg-TJ` - Tajik, `tr-TR` - Turkish, `tk` - Turkmen, `uk-UA` - Ukrainian, `ur` - Urdu, `uz-UZ` - Uzbek, `vi-VN` - Vietnamese, `xh` - Xhosa, `yo` - Yoruba, `zu` - Zulu

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://weather.cit.api.here.com//weather/1.0
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/report-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/here/master/_listings/here/report-json-get-openapi.md
x-common:
- type: x-blog-rss
  url: https://developer.here.com/blog/feed
- type: x-github
  url: https://github.com/heremaps
- type: x-postman-collection
  url: https://github.com/heremaps/postman-collections
- type: x-api-gallery
  url: http://healthcare.gov.api.gallery.streamdata.io
- type: x-api-stack
  url: http://here.stack.network
- type: x-blog
  url: https://developer.here.com/blog
- type: x-crunchbase
  url: https://crunchbase.com/organization/here-inc
- type: x-developer
  url: https://developer.here.com
- type: x-email
  url: dirk.popp@here.com
- type: x-email
  url: sebastian.kurme@here.com
- type: x-email
  url: jordan.stark@here.com
- type: x-email
  url: amy.stupavsky@here.com
- type: x-email
  url: minna.laub@here.com
- type: x-email
  url: stefanie.sirc@here.com
- type: x-email
  url: rachel.kuta@here.com
- type: x-email
  url: laurel.davis-lyons@here.com
- type: x-email
  url: linda.bradley@here.com
- type: x-email
  url: press@here.com
- type: x-twitter
  url: https://twitter.com/here
- type: x-website
  url: https://here.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---
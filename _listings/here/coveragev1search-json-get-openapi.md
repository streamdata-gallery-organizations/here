---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Public Transit API Transit Coverage Within a City
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
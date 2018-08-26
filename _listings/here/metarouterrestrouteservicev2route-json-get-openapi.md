---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Public Transit API Avoid Transit Routes Involving Transfers
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
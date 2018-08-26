---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Routing API Many to many matrix routing
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
  version: 1.0.0
host: route.cit.api.here.com
basePath: /routing/7.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
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
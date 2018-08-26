---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Traffic API Traffic Flow Availability Data
  description: |-
    *Flow availability requests allow you to see what traffic flow coverage exists in the current Traffic API.*

    T<i></i>he Server also supports an XML response.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  version: 1.0.0
host: tiles.traffic.cit.api.here.com
basePath: /traffic/6.0/tiles/8/133/86/256
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
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
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
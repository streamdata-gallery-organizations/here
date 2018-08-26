---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Map Tile API Terrain Map
  description: |-
    *Request a terrain map tile*

    Terrain map tile are available by passing `terrain.day` in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
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
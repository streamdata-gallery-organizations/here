---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Map Tile API Color-reduced Transit Map
  description: |-
    *Request a color-reduced map tile with public transport*

    Color-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.



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
---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Map Image API Map Image with Polylines
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
  version: 1.0.0
host: image.maps.cit.api.here.com
basePath: /mia/1.6
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
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
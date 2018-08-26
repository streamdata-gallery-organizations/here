---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Venue Maps Venue Clusters within a Bounding Box
  description: |-
    *Request an overview of the number venues across a large area*

    A bounding box is specified using the `bbox` parameter in the request URL.



    * **bbox**  `bbox`
     \- A type of spatial filter. A bounding box specifies the top-right and bottom left corners of an area to search.    e.g. `52.515,13.377;52.134,13.978`

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  version: 1.0.0
host: signature.venue.maps.cit.api.here.com
basePath: /venues/signature
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1:
    get:
      summary: Venue Clusters within a Bounding Box
      description: |-
        *Request an overview of the number venues across a large area*

        A bounding box is specified using the `bbox` parameter in the request URL.



        * **bbox**  `bbox`
         \- A type of spatial filter. A bounding box specifies the top-right and bottom left corners of an area to search.    e.g. `52.515,13.377;52.134,13.978`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: V1Get3
      x-api-path-slug: v1-get
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
      - Venue
      - Clusters
      - Within
      - Bounding
      - Box
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
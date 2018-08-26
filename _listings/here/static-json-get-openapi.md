---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Route Match Extension API Platform Static Data
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
  version: 1.0.0
host: pde.cit.api.here.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /static.json:
    get:
      summary: Platform Static Data
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
      operationId: StaticJsonGet
      x-api-path-slug: static-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: content
      - in: query
        name: region
      - in: query
        name: release
      responses:
        200:
          description: OK
      tags:
      - Platform
      - Static
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
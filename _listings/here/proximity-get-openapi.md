---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Custom Location Extension API Find the Five Nearest Locations
  description: |-
    *Request a list of user-defined locations within a circle around a fixed point*

    The search uses the `proximity` endpoint. The definition of the location and limit of the search is specified using  `coord` and `radius` parameters, and the number of results returned limited by adding the `limit` parameter to the request URL.



    * **layerId**  `text`
     \- Unique indicator used to retrieve a dataset

    * **coord**  `latlng`
     \- Center of the proximity search

    * **radius**  `number`
     \- width of the search corridor

    * **limit**  `number`
     \- The limit of the number of items contained in the response.

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  version: 1.0.0
host: customlocation.cit.api.here.com
basePath: /v1/search
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /jobs/puwWrv32YOU24y8MNoUr793chFAI36aC:
    get:
      summary: Get Job
      description: "*Request the status of a batch geocoder job*\n\nTo check the status,
        make a request to the `jobs` endpoint  appending the `requestId` and using
        the parameter `action=status `\n  \n\n\n\n* **action**  `enum`\n \\- Type
        of request  \n\n Valid values are : `cancel`, `runs`, `status`\n\n* **app_code**
        \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an `app_code` with every request.
        \ \n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
        used for the authentication of the client application.    You must include
        an `app_id` with every request."
      operationId: getJob
      x-api-path-slug: jobspuwwrv32you24y8mnour793chfai36ac-get
      parameters:
      - in: query
        name: action
      - in: query
        name: app_code
      - in: query
        name: app_id
      responses:
        200:
          description: OK
      tags:
      - Job
  /jobs:
    post:
      summary: Add Jobs
      description: "* Start asynchronously geocoding a large set of addresses in one
        batch*\n\nSubmit an HTTP POST request with `action=run` and attach the input
        data to the body. \n  \n\n\n\n* **gen**  `number`\n \\- Enables/disables backward
        incompatible behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64
        URL-safe encoded string used for the authentication of the client application.
        \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
        \\- A 20 byte Base64 URL-safe encoded string used for the authentication of
        the client application.    You must include an `app_code` with every request.\n\n*
        **action**  `enum`\n \\- Type of request\n\n Valid values are : `cancel`,
        `run`, `status`\n\n* **mailto**  `text`\n \\- Email address where completion
        notification is sent.\n\n* **header**  `enum`\n \\- If `true`, a header row
        is included before the results in the output.  \n\n Valid values are : `false`,
        `true`\n\n* **indelim**  `text`\n \\- \n\n* **outdelim**  `text`\n \\- \n\n*
        **outcols**  `text`\n \\- \n\n* **outputCombined**  `enum`\n \\- \n\n Valid
        values are : `true`, `false`"
      operationId: addJob
      x-api-path-slug: jobs-post
      parameters:
      - in: query
        name: action
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: gen
      - in: query
        name: header
      - in: query
        name: indelim
      - in: query
        name: mailto
      - in: query
        name: outcols
      - in: query
        name: outdelim
      - in: query
        name: outputCombined
      responses:
        200:
          description: OK
      tags:
      - Job
  /bbox:
    get:
      summary: Find Locations within a Bounding Box
      description: |-
        *Request a list of user-defined locations within a defined area*

        The request uses the `bbox` endpoint, and the bounding box is specified by adding the `bbox` parameter to the request URL.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **bbox**  `bbox`
         \- Restricts results to be found within this bounding box

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: BboxGet2
      x-api-path-slug: bbox-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: bbox
      - in: query
        name: layerId
      responses:
        200:
          description: OK
      tags:
      - Find
      - Locations
      - Within
      - Bounding
      - Box
  /attribute:
    get:
      summary: Filtering by Custom Attributes
      description: |-
        *Request a list of user-defined locations based on their attribute values*

        An attribute-based search is requested using the `attribute` endpoint and by adding the `query` parameter to the request URL.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **query**  `text`
         \- The query to retrieve

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: AttributeGet
      x-api-path-slug: attribute-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: layerId
      - in: query
        name: query
      responses:
        200:
          description: OK
      tags:
      - Filtering
      - By
      - Custom
      - Attributes
  /proximity:
    get:
      summary: Find the Five Nearest Locations
      description: |-
        *Request a list of user-defined locations within a circle around a fixed point*

        The search uses the `proximity` endpoint. The definition of the location and limit of the search is specified using  `coord` and `radius` parameters, and the number of results returned limited by adding the `limit` parameter to the request URL.



        * **layerId**  `text`
         \- Unique indicator used to retrieve a dataset

        * **coord**  `latlng`
         \- Center of the proximity search

        * **radius**  `number`
         \- width of the search corridor

        * **limit**  `number`
         \- The limit of the number of items contained in the response.

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: ProximityGet2
      x-api-path-slug: proximity-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: coord
      - in: query
        name: layerId
      - in: query
        name: limit
      - in: query
        name: radius
      responses:
        200:
          description: OK
      tags:
      - Find
      - Five
      - Nearest
      - Locations
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
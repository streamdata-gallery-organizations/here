---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Geocoder API Multi-reverse Geocode Addresses
  description: "*Request the addresses of up to one hundred locations with one multi-reverse
    geocoding request*\n\nThe body of the HTTP POST request contains the coordinates
    and optional radius in the `prox` parameter and an optional numeric identifier
    in the `id` parameter as plain text, one line per pair of coordinates. The identifier
    associates each result with the corresponding input. If no id is provided the
    system creates one starting with 0.\n  \n\n\n\n* **mode**  `enum`\n \\- Search
    for prominent landmarks nearby  \n\n Valid values are : `retrieveAddresses`, `retrieveAreas`,
    `retrieveLandmarks`, `retrieveAll`, `trackPosition`\n\n* **gen**  `number`\n \\-
    Enables/disables backward incompatible behavior in the API\n\n* **app_id**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_id` with every request.\n\n* **app_code**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_code` with every request.\n\n*
    **Content-Type**  `header`\n\n  Accept any content in return\n\n* **Cache-Control**
    \ `header`\n\n  Ensure that the request is always passed to server so that latest
    response is retrieved"
  version: 1.0.0
host: geocoder.cit.api.here.com
basePath: /6.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /geocode.json:
    get:
      summary: Geocode using partial address information
      description: "*Request the latitude, longitude and details of an address based
        on partial address information*\n\nThis example shows a structured (qualified)
        geocoding request using the `geocode` endpoint. In this structured request
        the data is provided in `country`, `city`, `street` and `housenumber` parameters
        in the request URL. Note that the street name misses the directional (\"W\")
        and also the street type. The omitted directional makes the query ambiguous
        and the response contains therefore two results: One address on West Randolph
        St and one on East Randolph St.\n  \n\n\n\n* **housenumber**  `text`\n \\-
        The house number or house name\n\n* **street**  `text`\n \\- The street name
        can include suite, apt and floor information.\n\n* **city**  `text`\n \\-
        City name\n\n* **country**  `text`\n \\- Specify the country or list of countries
        using the country code (3 bytes, ISO 3166-1-alpha-3) or the country name\n\n*
        **gen**  `number`\n \\- Enables/disables backward incompatible behavior in
        the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string
        used for the authentication of the client application.    You must include
        an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an `app_code` with every request."
      operationId: GeocodeJsonGet5
      x-api-path-slug: geocode-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: city
      - in: query
        name: country
      - in: query
        name: gen
      - in: query
        name: housenumber
      - in: query
        name: street
      responses:
        200:
          description: OK
      tags:
      - Geocode
      - Using
      - Partial
      - Address
      - Information
  /reversegeocode.json:
    get:
      summary: Reverse Geocode Landmarks
      description: |-
        *Request details of landmarks near to a given latitude and longitude*

        Landmark reverse geocoding requests can be made using the `reversegeocode` endpoint, specifying the parameter `mode=retrieveLandmarks`, and adding the `prox` parameter to the request URL.  Consult the  Geocoder API Reference for a full list of available landmark types.



        * **prox**  `prox`
         \- A type of spatial filter. Proximity specifies a circle to search using a latitude, a longitude, and a radius in meters.    e.g. `52.515,13.377,100`

        * **mode**  `enum`
         \- Type of search invoked. Search for streets, administrative areas or landmarks, or a combination of all three

         Valid values are : `retrieveAddresses`, `retrieveAreas`, `retrieveLandmarks`, `retrieveAll`, `trackPosition`

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

        * **gen**  `number`
         \- Enables/disables backward incompatible behavior in the API
      operationId: ReversegeocodeJsonGet4
      x-api-path-slug: reversegeocode-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: gen
      - in: query
        name: mode
      - in: query
        name: prox
      responses:
        200:
          description: OK
      tags:
      - Reverse
      - Geocode
      - Landmarks
  /multi-reversegeocode.json:
    post:
      summary: Multi-reverse Geocode Addresses
      description: "*Request the addresses of up to one hundred locations with one
        multi-reverse geocoding request*\n\nThe body of the HTTP POST request contains
        the coordinates and optional radius in the `prox` parameter and an optional
        numeric identifier in the `id` parameter as plain text, one line per pair
        of coordinates. The identifier associates each result with the corresponding
        input. If no id is provided the system creates one starting with 0.\n  \n\n\n\n*
        **mode**  `enum`\n \\- Search for prominent landmarks nearby  \n\n Valid values
        are : `retrieveAddresses`, `retrieveAreas`, `retrieveLandmarks`, `retrieveAll`,
        `trackPosition`\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible
        behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\-
        A 20 byte Base64 URL-safe encoded string used for the authentication of the
        client application.    You must include an `app_code` with every request.\n\n*
        **Content-Type**  `header`\n\n  Accept any content in return\n\n* **Cache-Control**
        \ `header`\n\n  Ensure that the request is always passed to server so that
        latest response is retrieved"
      operationId: MultiReversegeocodeJsonPost2
      x-api-path-slug: multireversegeocode-json-post
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: header
        name: Cache-Control
      - in: header
        name: Content-Type
      - in: query
        name: gen
      - in: query
        name: mode
      responses:
        200:
          description: OK
      tags:
      - Multi-reverse
      - Geocode
      - Resses
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
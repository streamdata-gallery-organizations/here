---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Geocoder API Geocode using partial address information
  description: "*Request the latitude, longitude and details of an address based on
    partial address information*\n\nThis example shows a structured (qualified) geocoding
    request using the `geocode` endpoint. In this structured request the data is provided
    in `country`, `city`, `street` and `housenumber` parameters in the request URL.
    Note that the street name misses the directional (\"W\") and also the street type.
    The omitted directional makes the query ambiguous and the response contains therefore
    two results: One address on West Randolph St and one on East Randolph St.\n  \n\n\n\n*
    **housenumber**  `text`\n \\- The house number or house name\n\n* **street**  `text`\n
    \\- The street name can include suite, apt and floor information.\n\n* **city**
    \ `text`\n \\- City name\n\n* **country**  `text`\n \\- Specify the country or
    list of countries using the country code (3 bytes, ISO 3166-1-alpha-3) or the
    country name\n\n* **gen**  `number`\n \\- Enables/disables backward incompatible
    behavior in the API\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded
    string used for the authentication of the client application.    You must include
    an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_code` with every request."
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
---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Weather API Multi-Language Support
  description: |-
    *Request current weather conditions in a foreign language*

    The language of the weather report is altered by adding the `language` parameter to the request URL.



    * **product**  `enum`
     \- The type of information to request

     Valid values are : `observation`, `forecast_7days`, `forecast_7days_simple`, `forecast_hourly`, `forecast_astronomy`, `alerts`, `nws_alerts`

    * **latitude**  `number`
     \- Latitude of the weather forecast.    e.g. `52.5159`

    * **longitude**  `number`
     \- Longitude of the weather forecast.    e.g. `13.3777`

    * **oneobservation**  `enum`
     \- A flag to indicate only one observation is required.

     Valid values are : `true`, `false`

    * **language**  `enum`
     \- The language for the observations within the forecast.

     Valid values are : `af-ZA` - Afrikaans, `sq` - Albanian, `am-ET` - Amharic, `ar` - Arabic, `as-IN` - Assamese, `az-AZ` - Azerbaijani, `eu` - Basque, `be` - Belarusian, `bn-BD` - Bengali-bd, `bn` - Bengali, `bs-BA` - Bosnian, `bg-BG` - Bulgarian, `ca` - Catalan, `zh-CN` - Chinese (PRC), `zh-HK` - Chinese (HK), `zh-TW` - Chinese (TW), `hr-HR` - Croatian, `cs-CZ` - Czech, `da-DK` - Danish, `nl-NL` - Dutch, `en` - English, `en-US` - English (US), `et-EE` - Estonian, `fa` - Farsi, `fa-AF` - Farsi-af, `fi-FI` - Finnish, `fr-CA` - French (CA), `fr` - French, `gl` - Galician, `ka-GE` - Georgian, `de` - German, `el-GR` - Greek, `gu-IN` - Gujarati, `ha` - Hausa, `he-IL` - Hebrew, `hi-IN` - Hindi, `hu-HU` - Hungarian, `is-IS` - Icelandic, `ig-NG` - Igbo, `id-ID` - Indonesian, `it` - Italian, `ja-JP` - Japanese, `kn-IN` - Kannada, `ks-IN` - Kashmiri, `kk-KZ` - Kazakh, `km-KH` - Khmer, `ky-KG` - Kirghiz, `ko-KR` - Korean, `lo-LA` - Lao, `lv-LV` - Latvian, `ln` - Lingala, `lt-LT` - Lithuanian, `mk-MK` - Macedonian, `mg-MG` - Malagasy, `ms-MY` - Malay, `ml-IN` - Malayalam, `mr-IN` - Marathi, `mn-MN` - Mongolian, `no-NO` - Norwegian, `or-IN` - Oriya, `pl-PL` - Polish, `pt-BR` - Portuguese (BR), `pt-PT` - Portuguese (PT), `pa` - Punjabi, `ps` - Pushto, `ro-RO` - Romanian, `ru-RU` - Russian, `sr-YU` - Serbian, `st` - Sesotho, `si-LK` - Sinhala, `sk-SK` - Slovak, `sl-SL` - Slovene, `es-ES` - Spanish, `es-US` - Spanish (US), `sw` - Swahili, `sv` - Swedish, `tl-PH` - Tagalog, `ta` - Tamil, `te-IN` - Telugu, `th-TH` - Thai, `tg-TJ` - Tajik, `tr-TR` - Turkish, `tk` - Turkmen, `uk-UA` - Ukrainian, `ur` - Urdu, `uz-UZ` - Uzbek, `vi-VN` - Vietnamese, `xh` - Xhosa, `yo` - Yoruba, `zu` - Zulu

    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  version: 1.0.0
host: weather.cit.api.here.com
basePath: /weather/1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /report.json:
    get:
      summary: Multi-Language Support
      description: |-
        *Request current weather conditions in a foreign language*

        The language of the weather report is altered by adding the `language` parameter to the request URL.



        * **product**  `enum`
         \- The type of information to request

         Valid values are : `observation`, `forecast_7days`, `forecast_7days_simple`, `forecast_hourly`, `forecast_astronomy`, `alerts`, `nws_alerts`

        * **latitude**  `number`
         \- Latitude of the weather forecast.    e.g. `52.5159`

        * **longitude**  `number`
         \- Longitude of the weather forecast.    e.g. `13.3777`

        * **oneobservation**  `enum`
         \- A flag to indicate only one observation is required.

         Valid values are : `true`, `false`

        * **language**  `enum`
         \- The language for the observations within the forecast.

         Valid values are : `af-ZA` - Afrikaans, `sq` - Albanian, `am-ET` - Amharic, `ar` - Arabic, `as-IN` - Assamese, `az-AZ` - Azerbaijani, `eu` - Basque, `be` - Belarusian, `bn-BD` - Bengali-bd, `bn` - Bengali, `bs-BA` - Bosnian, `bg-BG` - Bulgarian, `ca` - Catalan, `zh-CN` - Chinese (PRC), `zh-HK` - Chinese (HK), `zh-TW` - Chinese (TW), `hr-HR` - Croatian, `cs-CZ` - Czech, `da-DK` - Danish, `nl-NL` - Dutch, `en` - English, `en-US` - English (US), `et-EE` - Estonian, `fa` - Farsi, `fa-AF` - Farsi-af, `fi-FI` - Finnish, `fr-CA` - French (CA), `fr` - French, `gl` - Galician, `ka-GE` - Georgian, `de` - German, `el-GR` - Greek, `gu-IN` - Gujarati, `ha` - Hausa, `he-IL` - Hebrew, `hi-IN` - Hindi, `hu-HU` - Hungarian, `is-IS` - Icelandic, `ig-NG` - Igbo, `id-ID` - Indonesian, `it` - Italian, `ja-JP` - Japanese, `kn-IN` - Kannada, `ks-IN` - Kashmiri, `kk-KZ` - Kazakh, `km-KH` - Khmer, `ky-KG` - Kirghiz, `ko-KR` - Korean, `lo-LA` - Lao, `lv-LV` - Latvian, `ln` - Lingala, `lt-LT` - Lithuanian, `mk-MK` - Macedonian, `mg-MG` - Malagasy, `ms-MY` - Malay, `ml-IN` - Malayalam, `mr-IN` - Marathi, `mn-MN` - Mongolian, `no-NO` - Norwegian, `or-IN` - Oriya, `pl-PL` - Polish, `pt-BR` - Portuguese (BR), `pt-PT` - Portuguese (PT), `pa` - Punjabi, `ps` - Pushto, `ro-RO` - Romanian, `ru-RU` - Russian, `sr-YU` - Serbian, `st` - Sesotho, `si-LK` - Sinhala, `sk-SK` - Slovak, `sl-SL` - Slovene, `es-ES` - Spanish, `es-US` - Spanish (US), `sw` - Swahili, `sv` - Swedish, `tl-PH` - Tagalog, `ta` - Tamil, `te-IN` - Telugu, `th-TH` - Thai, `tg-TJ` - Tajik, `tr-TR` - Turkish, `tk` - Turkmen, `uk-UA` - Ukrainian, `ur` - Urdu, `uz-UZ` - Uzbek, `vi-VN` - Vietnamese, `xh` - Xhosa, `yo` - Yoruba, `zu` - Zulu

        * **app_id**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

        * **app_code**  `text`
         \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
      operationId: ReportJsonGet10
      x-api-path-slug: report-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: language
      - in: query
        name: latitude
      - in: query
        name: longitude
      - in: query
        name: oneobservation
      - in: query
        name: product
      responses:
        200:
          description: OK
      tags:
      - Multi-Language
      - Support
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
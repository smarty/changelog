# [.Net SDK](https://www.smarty.com/docs/sdk/dotnet)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [9.0.0] - 2025-06-20
- us-autocomplete
  - Removed support for deprecated api (use us-autocomplete-pro)
- Removed .withLicense from examples. This is an edge case that is rarely used.
- us-reverse-geo-api
  - Added support for SmartyKey

## [8.19.1] - 2025-05-12
- Added administrative_area_iso2 to international-street.
- Removed .withLicense from examples. Not needed if there is only one license and is confusing to most sdk users.

## [8.18.3] - 2024-11-06
- added support for custom parameters to client requests
- standardized the examples

## [8.18.2] - 2024-10-30
- international-street-api
  - Max results can now be set properly

## [8.18.1] - 2024-10-18
- international-street-api
  - Added new return fields additionalContent
    - deliveryInstallation
    - deliveryInstallationType
    - deliveryInstallationQualifierName
    - route
    - routeNumber
    - routeType

## [8.18.0] - 2024-09-30
- us-address-enrichment-api
  - Added address search

## [8.17.0] - 2024-08-16
- us-address-enrichment-api
  - Added support for geo reference
  - Added support for secondary data and secondary count

## [8.16.3] - 2024-07-03

- International Autocomplete API
  - Added two new fields to expose the administrative area long name and short (abbreviated) form:
    - administrative_area_short
    - administrative_area_long


## [8.16.2] - 2024-06-19

- US Enrichment API
  - Supports GeoReference dataset
  - Supports ETag for all datasets
  - Added support for include and exclude for Property dataset
  - Added the Universal call to support any dataset
  - Added sample code for GeoReference and Universal calls.
  - Enhanced Property sample code and added comments.
- US Street API and US Zipcode API
  - Added support for the Connecticut compatibility parameter


## [8.16.1] - 2024-03-21

### Changed:

- Fixed urlPrefix bug related to retries

## [8.16.0] - 2023-01-30

### Changed:

- Added Enrichment API capabilities

## [8.15.2] - 2023-11-14

### Changed:

- Updated International Autocomplete SDK example license value with correct value for v2


## [8.15.1] - 2023-11-14

### Changed:

- Updated US Autocomplete Pro SDK example to reflect correct use of Preferred City filter


## [8.15.0] - 2023-11-10

### Changed:

- Update International Autocomplete to v2
 - Change default endpoint of international-autocomplete-api to: "https://international-autocomplete.api.smarty.com/v2/lookup"
 - Remove `super-administrative-area` and `sub-administrative-area` fields from `Candidate`
 - Add `entries` (int) , `address_text` (string), and `address_id` (string) fields to `Candidate`
  - Add functionality to append `address_id` to URL path, not as query parameter
 - Remove `distance` , `geolocation` , `include_only_administrative_area` , `latitude` , and `longitude` fields from `Lookup`
 - Remove `international_geolocate_type`
 - In `international_autocomplete/client` `send()` function, add check to ensure i) `country` field on lookup is set and ii) `search` || `address_id` field is set
 - Update unit tests to cover behavior above

## [8.14.1] - 2023-10-26

### Changed:

- Added format field to us-street api.
- Changed default domain for all apis to *.api.smarty.com (was *.api.smartystreets.com). This change could affect firewall rules that allowed only the previous domain name

## [8.14.0] - 2023-07-06

### Changed:

- Added smarty_key field to us-street api.


## [8.13.19] - 2023-06-27

### Changed:

- Added "source" input and output fields to US Reverse Geo.


## [8.13.18] - 2023-02-17

### Changed:

- Added matching strategy support in the US Extract api client


## [8.13.17] - 2023-01-25

### Changed:

- Added new constants in international-autocomplete-api for use with the geolocation parameter:
    - "adminarea", "locality"


## [8.13.16] - 2023-01-24

### Changed:

- Added new input fields in international-autocomplete-api:
    - distance, geolocation, latitude, longitude
- Added new fields in international-autocomplete-api results:
    - super_administrative_area, sub_administrative_area


## [8.13.12] - 2022-11-08

### Changed:

- Added new fields in international-street:
    - administrative_area_short, administrative_area_long, level_type, level_number


## [8.13.8] - 2022-05-10

### Changed:

- US Street examples default to us-core-cloud license.


## [8.13.7] - 2022-04-07

### Changed:

- Content type being set directly on the request rather than the header.


## [8.13.6] - 2022-04-06

### Changed:

- Sleep for 5 seconds on 429 status code.


## [8.13.5] - 2022-03-04

### Changed:

- Add Content-Type when sending a batch.


## [8.13.4] - 2022-03-02

### Changed:

- Messages in US Street examples are more accurate pertaining to address validity.


## [8.13.3] - 2022-01-04

### Changed:

- Default candidates is 5 for enhanced matching.


## [8.13.2] - 2021-12-14

### Changed:

- Code to access static credentials in US Autocomplete Pro provided in example.


## [8.13.1] - 2021-11-22

### Changed:

- Docker build uses mcr rather than dockerhub
- Fixes to how filters are delimited in US Autocomplete Pro


## [8.13.0] - 2021-10-15

### Changed:

- Support for International Autocomplete API.


## [8.12.0] - 2021-09-23

### Changed:

- Source field added to US Autocomplete Pro lookup.


## [8.11.3] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [8.11.2] - 2021-08-13

### Changed:

- Autocomplete Pro example leverages proper "none" geolocation type.


## [8.11.1] - 2021-08-09

### Changed:

- Corrected geolocation type "none".


## [8.11.0] - 2021-07-14

### Changed:

- New match strategy "enhanced".


## [8.10.2] - 2021-07-13

### Changed:

- Syntax errors resolved in examples.


## [8.10.1] - 2021-07-06

### Changed:

- Removed match_mode, renamed match_details to enhanced_match.


## [8.10.0] - 2021-06-11

### Changed:

- License field descriptions in the examples.
- US Street enhanced matching integration fields in Analysis.


## [8.9.0] - 2021-03-23

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`
- Functionality added to handle the US Autocomplete Pro API.


## [8.8.0] - 2021-03-12

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`

## [8.7.1] - 2020-10-19

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.

## [8.7.0] - 2020-10-17

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.

## [8.6.1] - 2020-09-30

### Changed:

- Fixed issue of InputID not being returned on batch lookups.

## [8.6.0] - 2020-08-21

### Changed:

- User can now specify the license to be used.

## [8.5.0] - 2020-03-17

### Changed:

- Incorporates Client-specific marker interfaces.

## [8.4.1] - 2020-02-06

### Changed:

- Documentation in streetapi-single to assist in creating custom url endpoint.

## [8.4.0] - 2019-12-03

### Changed:

- Added custom header sender.

## [8.3.1] - 2019-11-25

### Changed:

- Fixed syntax error in international street example.
- Comment added to clarify match strategy.


## [8.3.0] - 2019-09-25

### Changed:

- Populated relevant input fields in examples.
- Added notes for readability.
- US Street example (.vb) updated to work with library.
- Made USStreetSingleAddressExample.vb compile.
- 'inputID' added to the response.


## [8.2.0] - 2019-03-13

### Changed:

- Added Match Strategy to examples.
- Moved changelog.
- 'changes' field added to International Street Analysis, Rootlevel created to assist.


## [8.1.1] - 2019-02-26

### Changed:

- Made Analysis compile.


## [8.1.0] - 2019-02-26

### Changed:

- Update integration test to check environment variables to enable alternative API URLs (`SMARTY_URL_INTERNATIONAL_STREET`, `SMARTY_URL_US_AUTOCOMPLETE`, `SMARTY_URL_US_EXTRACT`, `SMARTY_URL_US_STREET`, `SMARTY_URL_US_ZIP`).
- Deprecated Analysis.IsEWS_Match


## [8.0.15] - 2019-01-15

### Changed:

- By default add `Accept-Encoding: gzip` header to request and handle gzipped response.


## [8.0.14] - 2018-09-18

### Changed:

- Settled on approach to leveraging docker to develop and publish.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-dotnet-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.14...HEAD
[8.0.15]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.14...8.0.15
[8.0.14]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.13...8.0.14
[Earlier]: https://github.com/smartystreets/smartystreets-dotnet-sdk/releases

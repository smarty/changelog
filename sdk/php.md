# [PHP SDK](https://www.smarty.com/docs/sdk/php)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
## [6.0.0] - 2025-01-23
- Added support for Basic Auth
- us-street-api
  - Default match is now set to Enhanced if not explicitly set.

## [5.11.1] - 2025-11-21
- us-enrichment-api
    - Moved financial_history to property/principal response.

## [5.11.0] - 2025-11-17
- international-street-api
    - Added geocode_classification metadata response

## [5.10.1] - 2025-11-11
- international-postal-code-api
    - Added support for International Postal Code API

## [5.9.0] - 2025-10-23
- us-street-api
    - Added support for component analysis.

## [5.8.0] - 2025-10-21
- us-street-api
    - Added custom query sender.

## [5.7.2] - 2025-09-22
- us-enrichment
    - Added features input parameter.
    - Added financial_history to property/principal data response.
- international-street
    - Added occupant_use to metadata in response.

## [5.7.1] - 2025-08-04
- us-enrichment-api
  - add support for new risk dataset
  - add support for ETag

## [5.6.0] - 2025-06-25
- use constants throughout for require statements
- us-reverse-geo-api
  - add support for SmartyKey

## [5.5.0] - 2025-05-09
- Added administrative_area_iso2 to international-street.

## [5.4.0] - 2025-04-30
- Added with customer header option
- Remove implicit nullable parameters.

## [5.3.0] - 2025-02-18
- us-address-enrichment-api
  - Added support for Matched Address


## [5.2.2] - 2024-12-17
- Added county_source parameter for the US Street Address API
- Added include and exclude parameters for the US Address Enrichment API
- Added addCustomParameter function for all APIs
- Added tests for the new addCustomParameter function
- Added Client Test for the US Autocomplete Pro API

## [5.2.1] - 2024-10-28
- international-street-api
  - Added new return fields 
    - additionalContent
    - deliveryInstallation
    - deliveryInstallationType
    - deliveryInstallationQualifierName
    - route
    - routeNumber
    - routeType

## [5.2.0] - 2024-09-10
- us-address-enrichment-api
  - Added Address Search Feature for the US Address Enrichment API
  - Resolved null array issue for the aliases entry in the Secondary Dataset of the US Address Enrichment API

## [5.1.0] - 2024-08-02
- us-address-enrichment-api
  - Added support for geo reference
  - Added support for secondary data and secondary count

## [5.0.3] - 2024-07-03

- International Autocomplete API
  - Added two new fields to expose the administrative area long name and short (abbreviated) form:
    - administrative_area_short
    - administrative_area_long


## [5.0.2] - 2024-06-17

### Changed:

- Fixed X-Forwarded-For header formatting.

## [5.0.1] - 2024-05-14

### Changed:

- Completed removing support for (deprecated) legacy autocomplete api
- Removed some echo statements going to standard out

## [5.0.0] - 2024-05-13

### Changed:

- Removed support for legacy autocomplete api
- Added support for the X-Forwarded-For (XFF) request header

## [4.19.3] - 2024-03-21

### Changed:

- Fixed urlPrefix bug related to retries

## [4.19.2] - 2024-03-19

### Changed:

- Updated return fields of `us-enrichment` to match the corresponding live api response

## [4.19.1] - 2023-11-21

### Changed:

- Internal testing fix

## [4.19.0] - 2023-11-21

### Changed:

- Implement support for US Enrichment API

## [4.18.2] - 2023-11-14

### Changed:

- Updated International Autocomplete SDK example license value with correct value for v2


## [4.18.1] - 2023-11-14

### Changed:

- Updated US Autocomplete Pro SDK example to reflect correct use of Preferred City filter


## [4.18.0] - 2023-11-10

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

## [4.17.1] - 2023-10-26

### Changed:

- Added format field to us-street api.
- Changed default domain for all apis to *.api.smarty.com (was *.api.smartystreets.com). This change could affect firewall rules that allowed only the previous domain name

## [4.17.0] - 2023-07-06

### Changed:

- Added smarty_key field to us-street api.


## [4.16.29] - 2023-06-27

### Changed:

- Added "source" input and output fields to US Reverse Geo.


## [4.16.28] - 2023-03-14

### Changed:

- Added match strategy to us-extract api.

## [4.16.27] - 2023-02-14

### Changed:


- Added new fields in international-autocomplete-api
  - super_administrative_area, sub_administrative_area

## [4.16.22] - 2022-11-08

### Changed:

- Added new fields in international-street:
    - administrative_area_short, administrative_area_long, level_type, level_number


## [4.16.21] - 2022-09-21

### Changed:

- Updated 429 error handling and messages.

## [4.16.18] - 2022-06-13

### Changed:

- Incremented version.


## [4.16.17] - 2022-06-13

### Changed:

- Updated README.md and LICENSE.md files.
- Fixed geolocation and zipcode functions.


## [4.16.16] - 2022-05-11

### Changed:

- Incremented version.


## [4.16.15] - 2022-05-11

### Changed:

- MyLogger utilizes PHP error log.


## [4.16.14] - 2022-05-10

### Changed:

- Incremented version.


## [4.16.13] - 2022-05-10

### Changed:

- US Street examples default to us-core-cloud license.


## [4.16.12] - 2022-04-20

### Changed:

- Incremented version.


## [4.16.11] - 2022-04-20

### Changed:

- Sleep for 5 seconds on 429 status code.


## [4.16.10] - 2022-03-23

### Changed:

- Incremented version.


## [4.16.9] - 2022-03-23

### Changed:

- Fixes bug in setting autocomplete result limit.


## [4.16.8] - 2022-03-02

### Changed:

- Incremented version.


## [4.16.7] - 2022-03-02

### Changed:

- Messages in US Street examples are more accurate pertaining to address validity.


## [4.16.6] - 2022-01-04

### Changed:

- Incremented version.


## [4.16.5] - 2022-01-04

### Changed:

- Default candidates is 5 for enhanced matching.


## [4.16.4] - 2021-12-15

### Changed:

- Incremented version.


## [4.16.3] - 2021-12-14

### Changed:

- Code to access static credentials in US Autocomplete Pro provided in example.


## [4.16.2] - 2021-11-22

### Changed:

- Fixes to how filters are delimited in US Autocomplete Pro.
- Incremented version.


## [4.16.1] - 2021-10-19

### Changed:

- Incremented version.


## [4.16.0] - 2021-10-19

### Changed:

- Support for International Autocomplete API.


## [4.15.1] - 2021-09-23

### Changed:

- Incremented version.


## [4.15.0] - 2021-09-23

### Changed:

- Source field added to US Autocomplete Pro lookup.


## [4.14.3] - 2021-08-20

### Changed:

- Incremented version.


## [4.14.2] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [4.14.1] - 2021-07-14

### Changed:

- Incremented version.


## [4.14.0] - 2021-07-14

### Changed:

- New match strategy "enhanced".


## [4.13.6] - 2021-07-06

### Changed:

- Incremented version.


## [4.13.5] - 2021-07-06

### Changed:

- Removed match_mode, renamed match_details to enhanced_match.


## [4.13.4] - 2021-06-11

### Changed:

- License field descriptions in the examples.
- US Street enhanced matching integration fields in Analysis.


## [4.13.3] - 2021-04-14

### Changed:

- Incremented version.


## [4.13.2] - 2021-04-14

### Changed:

- Simultaneous load issue resolved.


## [4.13.1] - 2021-03-23

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`
- Functionality added to handle the US Autocomplete Pro API.


## [4.12.1] - 2021-03-12

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`


## [4.11.3] - 2020-11-23

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.


## [4.11.1] - 2020-11-06

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.


## [4.10.1] - 2020-08-20

### Changed:

- User can now specify the license to be used.


## [4.9.1] - 2020-07-30

### Changed:

- Returning StatusCodes in the results.


## [4.8.0] - 2019-11-25

### Changed:

- Populated relevant input fields in example lookups.
- Input ID added to results.
- Comment added to clarify match strategy.
- Changes to accomodate php updates.


## [4.7.1] - 2019-03-14

### Changed:

- Incremented version.


## [4.7.0] - 2019-03-13

### Changed:

- Added match strategy to examples.
- Changelog moved.
- Added 'changes' to international street analysis, Rootlevel created to accomodate.


## [4.6.2] - 2019-02-25

### Changed:

- Extra build.


## [4.6.1] - 2019-02-25

### Changed:

- Extra build.


## [4.6.0] - 2019-02-25

### Changed:

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)
- Update integration test to check environment variables to enable alternative API URLs (`SMARTY_URL_INTERNATIONAL_STREET`, `SMARTY_URL_US_AUTOCOMPLETE`, `SMARTY_URL_US_EXTRACT`, `SMARTY_URL_US_STREET`, `SMARTY_URL_US_ZIP`).


## [4.5.7] - 2019-01-15

### Changed:

- By default add `Accept-Encoding: gzip` header to request and handle gzipped response.


## [4.5.6] - 2018-09-18

### Changed:

- Standardized `Makefile`.
- Push latest commits to repo when running `make publish`.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-php-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-php-sdk/compare/4.5.6...HEAD
[4.5.6]: https://github.com/smartystreets/smartystreets-php-sdk/compare/4.5.5...4.5.6
[Earlier]: https://github.com/smartystreets/smartystreets-php-sdk/releases

# [PHP SDK](https://www.smarty.com/docs/sdk/php)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [4.17.1] - 2023-10-26

### Changed:

- Added format field to us-street api.


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

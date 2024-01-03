# [Ruby SDK](https://www.smarty.com/docs/sdk/ruby)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [5.17.0] - 2024-01-03

### Changed:

- Add support for the US Enrichment API

## [5.16.2] - 2023-11-17

### Changed:

- Removed geolocation type require from International Autocomplete

## [5.16.1] - 2023-11-14

### Changed:

- Updated International Autocomplete SDK example license value with correct value for v2
- Updated US Autocomplete Pro SDK example to reflect correct use of Preferred City filter


## [5.16.0] - 2023-11-10

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

## [5.15.4] - 2023-11-07

### Changed:

- Added other necessary `international-autocomplete` requires lines


## [5.15.3] - 2023-11-07

### Changed:

- Added `international-autocomplete` to `smartystreets_ruby_sdk.rb`


## [5.15.2] - 2023-10-24

### Changed:

- Removed unused value in us-street api.


## [5.15.1] - 2023-10-24

### Changed:

- Added format field to us-street api.


## [5.15.0] - 2023-07-06

### Changed:

- Added smarty_key field to us-street api.


## [5.14.20] - 2023-06-27

### Changed:

- Added "source" input and output fields to US Reverse Geo.


## [5.14.19] - 2023-03-08

### Changed:

- Added match strategy to us-extract api.

## [5.14.18] - 2023-02-14

### Changed:

- Added new fields in international-autocomplete-api:
  - max_results, distance, geolocation, latitude, longitude
- Added new fields in international-autocomplete-api results:
  - super_administrative_area, sub_administrative_area

## [5.14.17] - 2022-11-08

### Changed:

- Added new fields in international-street:
    - administrative_area_short, administrative_area_long, level_type, level_number


## [5.14.14] - 2022-09-19

### Changed:

- Adding handling for "retry-able" HTTP responses.
- Reading the "Retry-After" header properly.
- A few more tests.

## [5.14.10] - 2022-05-10

### Changed:

- US Street examples default to us-core-cloud license.


## [5.14.9] - 2022-04-20

### Changed:

- Sleep for 5 seconds on 429 status code.


## [5.14.8] - 2022-04-06

### Changed:

- Properly handling result of international autocomplete lookup.


## [5.14.7] - 2022-03-09

### Changed:

- Lookup candidate defaults to 0 to avoid client changing intentional values.


## [5.14.6] - 2022-03-02

### Changed:

- Messages in US Street examples are more accurate pertaining to address validity.


## [5.14.5] - 2022-01-12

### Changed:

- Default candidates is 5 for enhanced matching.


## [5.14.4] - 2021-12-14

### Changed:

- International Autocomplete Example has its own class.
- Code to access static credentials in US Autocomplete Pro provided in example.


## [5.14.3] - 2021-11-24

### Changed:

- Fixed broken tests.


## [5.14.2] - 2021-11-24

### Changed:

- Fixes to how filters are delimited in US Autocomplete Pro.


## [5.14.1] - 2021-10-28

### Changed:

- Default timeout for opening HTTP connection defaults to same as read timeout.


## [5.14.0] - 2021-10-05

### Changed:

- Support for International Autocomplete API.


## [5.13.0] - 2021-09-23

### Changed:

- Updated dependencies.
- Source field added to US Autocomplete Pro Lookup.


## [5.12.1] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [5.12.0] - 2021-07-14

### Changed:

- New match strategy "enhanced".


## [5.11.2] - 2021-07-06

### Changed:

- Removed match_mode, renamed match_details to enhanced_match.


## [5.11.1] - 2021-06-15

### Changed:

- WithLicenses calls in examples changed to have acceptable parameter array type.


## [5.11.0] - 2021-06-11

### Changed:

- License field descriptions in the examples.
- US Street enhanced matching integration fields in Analysis.


## [5.10.0] - 2021-03-12

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`
- Functionality added to handle the US Autocomplete Pro API.


## [5.9.2] - 2020-11-30

### Changed:

- Checking if candidates are nil before iterating in International Street Client.


## [5.9.1] - 2020-11-23

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.


## [5.9.0] - 2020-10-29

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.


## [5.8.0] - 2020-08-25

### Changed:

- User can now specify the license to be used.


## [5.7.1] - 2019-11-25

### Changed:

- Comment added to clarify match strategy.


## [5.7.0] - 2019-03-13

### Changed:

- Added Changes structure to InternationalStreet Analysis, created Rootlevel structure to accomodate.


## [5.6.2] - 2019-03-04

### Changed:

- Revert "Renamed log method for fake logging."


## [5.6.1] - 2019-02-28

### Changed:

- Match strategy added to examples.
- Moved changelog.


## [5.6.0] - 2019-02-25

### Changed:

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)
- Using `warn` instead of `log` to avoid conflict with builtin function.


## [5.5.4] - 2018-09-18

### Changed:

- Standardized `Makefile`.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-ruby-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-ruby-sdk/compare/5.5.4...HEAD
[5.5.4]: https://github.com/smartystreets/smartystreets-ruby-sdk/compare/5.5.3...5.5.4
[Earlier]: https://github.com/smartystreets/smartystreets-ruby-sdk/releases

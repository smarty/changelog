# [Python SDK](https://www.smarty.com/docs/sdk/python)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [4.12.0] - 2023-07-06

### Changed:

- Added smarty_key field to us-street api.


## [4.11.17] - 2023-06-27

### Changed:

- Added "source" input and output fields to US Reverse Geo.


## [4.11.16] - 2023-03-15

### Changed:

- Added code to make the MatchType enum backward compatible with hardcoded string values

## [4.11.15] - 2023-03-11

### Changed:

- Make compatible with Python 3.10 again.

## [4.11.14] - 2023-03-10

### Changed:

- Added match strategy to us-extract api.
- Require Python 3.11

## [4.11.12] - 2023-01-25

### Changed:

- Change the max timeout to reflect that it is in seconds, not milliseconds and make the default 10 seconds.

## [4.11.11] - 2023-01-25

### Changed:

- Using python 'with' syntax to ensure session response objects don't hang on to file handles when there are errors.

## [4.11.10] - 2023-01-25

### Changed:

- Added new fields in international-autocomplete-api results:
  - super_administrative_area, sub_administrative_area

- Added new fields in international-autocomplete-api:
  - max_results, distance, geolocation, latitude, longitude

## [4.11.9] - 2022-11-08

### Changed:

- Added new fields in international-street:
    - administrative_area_short, administrative_area_long, level_type, level_number


## [4.10.12] - 2022-09-15

### Changed:

- Handle rate limiting (429) a little more gracefully.
- When a 429 error response is received, we want to surface the real error message from the server.


## [4.10.11] - 2022-05-10

### Changed:

- US Street examples default to us-core-cloud license.


## [4.10.10] - 2022-05-04

### Changed:

- Multiple results returned in the US Reverse Geo.


## [4.10.9] - 2022-04-19

### Changed:

- Makefile uses python3 exclusively rather than python.


## [4.10.8] - 2022-04-19

### Changed:

- Sleep for 5 seconds on 429 status code.


## [4.10.7] - 2022-03-23

### Changed:

- Properly getting candidates from international autocomplete response.


## [4.10.6] - 2022-03-02

### Changed:

- Messages in US Street examples are more accurate pertaining to address validity.


## [4.10.5] - 2022-01-11

### Changed:

- Default candidates is 5 for enhanced matching.


## [4.10.4] - 2021-12-14

### Changed:

- Code to access static credentials in US Autocomplete Pro provided in example.


## [4.10.3] - 2021-11-18

### Changed:

- Fixes to how filters are delimited in US Autocomplete Pro.


## [4.10.2] - 2021-10-05

### Changed:

- Fixed misplaced comma.


## [4.10.1] - 2021-10-05

### Changed:

- Include International Autocomplete package in setup.


## [4.10.0] - 2021-10-05

### Changed:

- Source field added to US Autocomplete Pro Lookup.
- Support for International Autocomplete API.


## [4.9.1] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [4.9.0] - 2021-07-15

### Changed:

- New match strategy "enhanced".


## [4.8.5] - 2021-07-06

### Changed:

- Removed match_mode, renamed match_details to enhanced_match.


## [4.8.4] - 2021-06-11

### Changed:

- US Street enhanced matching integration fields in Analysis.
- Makefile updates for latest python version.


## [4.8.3] - 2021-05-26

### Changed:

- Fixes to the way licenses are handled.


## [4.8.2] - 2021-05-26

### Changed:

- License field descriptions in the examples.
- More output fields in us-street examples.


## [4.8.1] - 2021-05-25

### Changed:

- Autocomplete Pro added to setup.
- Using key instead of auth-id for embedded (website) key authentication.


## [4.8.0] - 2021-03-23

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`
- Functionality added to handle the US Autocomplete Pro API.


## [4.7.3] - 2021-02-24

### Changed:

- dpv_no_stat field added on the response.


## [4.7.2] - 2020-11-20

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.


## [4.7.1] - 2020-10-30

### Changed:

- Updates to setup file, making US Reverse Geo visible.


## [4.7.0] - 2020-10-30

### Changed:

- Update to examples to accurately represent match field accepted inputs.
- Functionality added to handle the new US Reverse Geocoding API.


## [4.6.1] - 2020-08-21

### Changed:

- Fixed broken tests surrounding mandatory population of street field.


## [4.6.0] - 2020-08-21

### Changed:

- Street field needs to be populated.
- User can now specify the license to be used.


## [4.5.0] - 2020-04-03

### Changed:

- Support configuring CA bundle & proxy via env vars. 


## [4.4.1] - 2020-02-26

### Changed:

- Fixed bug that made the autocomplete client crash if there are no suggestions in the response.

## [4.4.0] - 2019-11-25

### Changed:

- Return input id with result.
- Comment added to clarify match strategy.


## [4.3.0] - 2019-06-05

### Changed:

- Populated relevant input fields in examples.
- New custom header option available in client builder.


## [4.2.0] - 2019-03-13

### Changed:

- Moved changelog.
- Changes structure added to analysis in international street API. Rootlevel created to accomodate.


## [4.1.0] - 2019-02-25

### Changed:

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)


## [4.0.1] - 2019-01-14

### Changed:

- Re-introduced dependency on twine for uploading new releases to PyPI.

## [4.0.0] - 2019-01-14

### Changed:

- Moved `__version__` variable to its own module to remove installation dependency on `requests` module.

## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-python-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-python-sdk/compare/4.0.1...HEAD
[4.0.1]: https://github.com/smartystreets/smartystreets-python-sdk/compare/4.0.0...4.0.1
[4.0.0]: https://github.com/smartystreets/smartystreets-python-sdk/compare/3.3.2...4.0.0
[Earlier]: https://github.com/smartystreets/smartystreets-python-sdk/releases

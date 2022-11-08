# [iOS SDK](https://www.smarty.com/docs/sdk/ios)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [8.10.18] - 2022-11-08

### Changes:

- Added new fields in international-street:
    - administrative_area_short, administrative_area_long, level_type, level_number


## [8.10.17] - 2022-09-12

### Changes:

- When a 429 error response is received, we want to surface the real error message from the server.

## [8.10.16] - 2022-07-20

### Changes:

- Fixed crash for bulk us-street-api when returning more than one candidate.

## [8.10.15] - 2022-05-10

### Changes:

- Incremented version.


## [8.10.14] - 2022-05-10

### Changes:

- US Street examples default to us-core-cloud license.


## [8.10.13] - 2022-04-20

### Changes:

- Incremented version.


## [8.10.12] - 2022-04-20

### Changes:

- Sleep for 5 seconds on 429 status code.


## [8.10.11] - 2022-04-11

### Changes:

- Incremented version.


## [8.10.10] - 2022-04-11

### Changes:

- Made fields in the US Street API public.


## [8.10.9] - 2022-03-02

### Changes:

- Incremented version.


## [8.10.8] - 2022-03-02

### Changes:

- Messages in US Street examples are more accurate pertaining to address validity.


## [8.10.7] - 2022-01-12

### Changes:

- Incremented version.


## [8.10.6] - 2022-01-12

### Changes:

- Default candidates is 5 for enhanced matching.


## [8.10.5] - 2021-12-15

### Changes:

- Incremented version.


## [8.10.4] - 2021-12-15

### Changes:

- Code to access static credentials in US Autocomplete Pro provided in example.


## [8.10.3] - 2021-11-11

### Changes:

- Removed redundant URL Encoding.


## [8.10.2] - 2021-10-21

### Changes:

- Incremented version.


## [8.10.1] - 2021-10-21

## Changes:

- Fixes to broken International Autocomplete Client tests.


## [8.10.0] - 2021-10-21

### Changes:

- Support for International Autocomplete API.


## [8.9.0] - 2021-09-23

### Changed:

- Ensuring proper URL encoding on US Autocomplete Pro requests.
- Source field added to US Autocomplete Pro lookup.


## [8.8.8] - 2021-08-20

### Changed:

- Incremented version.


## [8.8.7] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [8.8.6] - 2021-07-08

### Changed:

- CodingKeys allows Analysis deserialization.


## [8.8.5] - 2021-07-07

### Changed:

- Incremented version.


## [8.8.4] - 2021-07-07

### Changed:

- Http response from the International API is properly written to output.


## [8.8.3] - 2021-07-06

### Changed:

- Incremented version.


## [8.8.2] - 2021-07-06

### Changed:

- Removed match_mode, renamed match_details to enhanced_match.


## [8.8.1] - 2021-06-11

### Changed:

- Incremented version.

## [8.8.0] - 2021-06-11

### Changed:

- US Street enhanced matching integration fields in Analysis.
- License field descriptions in the examples.


## [8.7.3] - 2021-05-07

### Changed:

- Incremented version.


## [8.7.2] - 2021-05-07

### Changed:

- Handling requests sent without internet connection.


## [8.7.1] - 2021-03-12

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`


## [8.6.5] - 2021-02-24

### Changed:

- Incremented version.


## [8.6.4] - 2021-02-24

### Changed:

- Percentage encoding is extended to all urlHostAllowed special characters.


## [8.6.3] - 2020-11-20

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.


## [8.6.1] - 2020-10-23

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.


## [8.5.1] - 2020-09-08

### Changed:

- User can now specify the license to be used.


## [8.4.3] - 2020-07-30

### Changed:

- Fixed Makefile


## [8.4.2] - 2020-07-30

### Changed:

- Fixed support for Swift Package Manager


## [8.4.1] - 2019-12-10

### Changed:

- Changes in Makefile to compile
- US-Autocomplete-Pro API added
- Comments in examples clarify match strategy


## [8.4.0] - 2019-10-07

### Changed:

- Contrained cd operations in Makefile
- Renamed directories
- Added paths to fix Package targets
- UI Samples added in Objective-C and Swift
- Only Shared Credentials allowed for appropriate use of sdk
- Objective-C samples included


## [8.3.3] - 2019-07-10

### Changed:

- Sender tools made public.
- Sender has more flexibility with nil returns.


## [8.3.2] - 2019-07-10

### Changed:

- Additional input fields in examples.


## [8.3.1] - 2019-07-10

### Changed:

- Incremented version.


## [8.3.0] - 2019-07-10

### Changed:

- Objective C examples created.


## [8.2.1] - 2019-07-10

### Changed:

- Incremented version.


## [8.2.0] - 2019-07-10

### Changed:

- Separated executables from library.

## [8.1.1] - 2019-07-10

### Changed:

- Incremented version.


## [8.1.0] - 2019-08-05

### Changed:

- Accept gzip encoded requests.


## [8.0.0] - 2019-07-01

### Changed:

- Library changed from Objective C to Swift.


## [7.7.3] - 2019-03-15

### Changed:

- Incremented version.


## [7.7.2] - 2019-03-15

### Changed:

- Incremented version.


## [7.7.1] - 2019-03-14

### Changed:

- Incremented version.


## [7.7.0] - 2019-03-14

### Changed:

- Changes field added to Analysis object. (Rootlevel added to accomodate)
- Changelog moved to separate repository.
- Match=invalid added to example.


## [7.6.7] - 2019-02-26

### Changed:

- Incremented version.


## [7.6.6] - 2019-02-26

### Changed:

- Incremented version.


## [7.6.5] - 2019-02-26

### Changed:

- Incremented version.


## [7.6.4] - 2019-02-26

### Changed:

- Incremented version.


## [7.6.3] - 2019-02-26

### Changed:

- Incremented version.


## [7.6.2] - 2019-02-26

### Changed:

- Incremented version.


## [7.6.1] - 2019-02-26

### Changed:

- Incremented version.


## [7.6.0] - 2019-02-26

### Changed:

- Deprecated EWS Match.
- Moved EWS Match to Metadata.


## [7.5.4] - 2018-09-24

### Changed:

- Now running `make` targets on the host environment.

## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-ios-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-ios-sdk/compare/7.5.4...HEAD
[7.5.4]: https://github.com/smartystreets/smartystreets-ios-sdk/compare/7.5.3...7.5.4
[Earlier]: https://github.com/smartystreets/smartystreets-ios-sdk/releases

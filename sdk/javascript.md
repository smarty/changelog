# [Javascript SDK](https://smartystreets.com/docs/sdk/javascript)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]


## [1.10.4] - 2021-08-23

### Changed:

- Lookup returned with response attached rather than response being returned.


## [1.10.3] - 2021-08-20

### Changed:

- Removed response parameter to comply with API response.


## [1.10.2] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [1.10.1] - 2021-08-19

### Changed:

- Bump patch version.


## [1.10.0] - 2021-08-19

### Changed:

- Updated dependencies.
- International Address Autocomplete API.


## [1.9.2] - 2021-07-06

### Changed:

- Removed match_mode, renamed match_details to enhanced_match.


## [1.9.1] - 2021-06-17

### Changed:

- No need to set the hostname for js client side since the browser takes care of this, defaults to showing client side example.


## [1.9.0] - 2021-06-11

### Changed:

- License field descriptions in the examples.
- US Street enhanced matching integration fields in Analysis.


## [1.8.1] - 2021-05-03

### Changed:

- Proper naming on the `coordinateLicense` field
- Naming changes in examples


## [1.8.0] - 2021-04-30

### Changed:

- Naming changes in examples
- Updated the way client is built in examples
- New `coordinateLicense` field in the US Street response


## [1.7.2] - 2021-03-12

### Changed:

- Latest dependencies
- Node tests
- Fixes to setting referer field


## [1.7.0] - 2021-03-05

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`

## [1.6.3] - 2020-12-21

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response

## [1.6.2] - 2020-12-10

### Changed:

- Fixed WithLicense functionality

## [1.6.1] - 2020-12-03

### Changed:

- Latest dependencies
- Updates to US Street Example

## [1.6.0] - 2020-10-08

### Changed:

- Functionality added to handle the new US Reverse Geocoding API

## [1.5.0] - 2020-08-14

### Changed:

- Latest Dependencies
- User can now specify the license to be used.

## [1.4.5] - 2020-06-17

### Changed:

- Preference to website keys in this SDK rather than authID and authToken
- Latest dependencies

## [1.4.4] - 2020-03-16

### Changed:

- Comments in US Street clarify match strategy
- Example code is more universally usable
- Latest dependencies

## [1.4.2] - 2019-11-05

### Changed:

- Added support for US Autocomplete Pro

### Changed:

- Nothing yet

## [1.1.7] - 2018-09-26

### Changed:

- Separated `clean` from `test` make target.

## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-javascript-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-javascript-sdk/compare/1.1.7...HEAD
[1.1.7]: https://github.com/smartystreets/smartystreets-javascript-sdk/compare/1.1.6...1.1.7
[Earlier]: https://github.com/smartystreets/smartystreets-javascript-sdk/releases

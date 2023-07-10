# [Javascript SDK](https://www.smarty.com/docs/sdk/javascript)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.2.0] - 2023-07-10

### Changed:

- Updated API url domains from `*.api.smartystreets.com` to `*.api.smarty.com`


## [2.1.1] - 2022-11-23

### Added:

- Adds note about authentication options with US Autocomplete Pro 


## [2.1.2] - 2023-04-18

### Changed:

- Reduced disclaimer font size

### Security:

- Bump minimatch from 3.0.4 to 3.1.2

## [2.1.1] - 2022-11-23

### Added:

- Adds note about authentication options with US Autocomplete Pro 


## [2.1.0] - 2022-11-09

### Added:

- Added new fields in international street results:
	- administrativeAreaShort, administrativeAreaLong, levelType, levelNumber


## [2.0.0] - 2022-07-26

### Changed:

- Enhanced retries for certain HTTP error codes
- Handles 429 retries more gracefully


## [1.13.7] - 2022-07-26

### Changed:

- Changed wording from "website keys" to "embedded keys"


## [1.13.6] - 2022-06-24


## [1.13.5] - 2022-06-24


## [1.13.4] - 2022-06-24

### Changed:

- Updated README and LICENSE


## [1.13.3] - 2022-05-25

### Changed:

- Removed unused dependencies.


## [1.13.2] - 2022-04-11

### Changed:

- Removed s3 code.


## [1.13.1] - 2022-04-08

### Changed:

- Latest dependencies:
	- node_modules/minimist


## [1.13.0] - 2022-04-07

### Changed:

- Replaced axios with axios-proxy-fix


## [1.12.0] - 2022-03-31

### Changed:

- Ability to set max results for international-autocomplete calls.


## [1.11.11] - 2022-02-21

### Changed:

- Latest dependencies:
	- node_modules/cached-path-relative
	- cached-path-relative
	- node_modules/pathval
	- node_modules/follow-redirects
	- node_modules/chokidar
	- anymatch
	- glob-parent
	- fsevents
	- node_modules/glob
	- node_modules/js-yaml
	- node_modules/log-symbols/node_modules/chalk
	- node_modules/mocha
	- node_modules/nanoid
	- node_modules/picomatch
	- node_modules/readdirp
	- node_modules/serialize-javascript
	- node_modules/workerpool
	- log-symbols
- Added dependencies:
	- node_modules/debug
	- node_modules/debug/node_modules/ms
	- node_modules/is-unicode-supported
	- dependencies
- Removed dependencies:
	- node_modules/is-fullwidth-code-point
	- node_modules/mocha/node_modules/debug
	- node_modules/mocha/node_modules/debug/node_modules/ms
	- node_modules/string-width
	- node_modules/string-width/node_modules/ansi-regex
	- node_modules/string-width/node_modules/strip-ansi
	- node_modules/wide-align


## [1.11.10] - 2022-01-18

### Changed:

- Latest dependencies:
	- node_modules/follow-redirects
- Removal of unnessecary dependencies.


## [1.11.8] - 2022-01-12

### Changed:

- Default candidates is 5 for enhanced matching.


## [1.11.7] - 2021-12-08

### Changed:

- Support for asynchronous API calls.


## [1.11.3] - 2021-10-20

### Changed:

- Reverted axios-retry to working version.


## [1.11.2] - 2021-10-07

### Changed:

- Updated axios-retry version.
- Updated to expect response to return 'candidates' key.


## [1.11.0] - 2021-09-23

### Changed:

- Delete trailing line in International Street Example and US Street Example.
- Source field added to US Autocomplete Pro lookup.


## [1.10.6] - 2021-09-07

### Changed:

- Updated new lookup parameters and tests.


## [1.10.5] - 2021-09-02

### Changed:

- npm audit fix.


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
